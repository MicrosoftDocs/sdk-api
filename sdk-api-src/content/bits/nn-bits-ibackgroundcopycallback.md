---
UID: NN:bits.IBackgroundCopyCallback
title: IBackgroundCopyCallback (bits.h)
description: Implement the IBackgroundCopyCallback interface to receive notification that a job is complete, has been modified, or is in error. Clients use this interface instead of polling for the status of the job.
helpviewer_keywords: ["IBackgroundCopyCallback","IBackgroundCopyCallback interface [BITS]","IBackgroundCopyCallback interface [BITS]","described","_drz_ibackgroundcopycallback","bits.ibackgroundcopycallback","bits/IBackgroundCopyCallback"]
old-location: bits\ibackgroundcopycallback.htm
tech.root: Bits
ms.assetid: e1aa6775-d1e5-4463-ae0f-32c0498881e1
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback, IBackgroundCopyCallback interface [BITS], IBackgroundCopyCallback interface [BITS],described, _drz_ibackgroundcopycallback, bits.ibackgroundcopycallback, bits/IBackgroundCopyCallback
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback
 - bits/IBackgroundCopyCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.h
api_name:
 - IBackgroundCopyCallback
---

# IBackgroundCopyCallback interface


## -description

Implement the 
<b>IBackgroundCopyCallback</b> interface to 
<a href="/windows/desktop/Bits/registering-a-com-callback">receive notification</a> that a job is complete, has been modified, or is in error. Clients use this interface instead of  <a href="/windows/desktop/Bits/polling-for-the-status-of-the-job">polling for the status of the job</a>.

## -inheritance

The <b>IBackgroundCopyCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBackgroundCopyCallback</b> also has these types of members:

## -remarks

To receive notifications, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> method to specify the interface pointer to your 
<b>IBackgroundCopyCallback</b> implementation. To specify which notifications you want to receive, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a> method.

BITS will call your callbacks as long as the interface pointer is valid. The notification interface is no longer valid when your application terminates; BITS does not persist the notify interface. As a result, your application's initialization process should call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">SetNotifyInterface</a> method on those existing jobs for which you want to receive notification.

BITS guarantees to call your callback at least once, even if the registration occurs after the event. For example, if you request notification of a job transfer after the transfer occurred, you will receive the job transferred callback. Also, if a job received a notification and the pointer is subsequently  no longer valid, that job would receive another notification if you later set the interface pointer on that job.

You must implement all methods of the 
<b>IBackgroundCopyCallback</b> interface. For example, if you do not register for the job modification callback, the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-jobmodification">JobModification</a> method must still return <b>S_OK</b>.

The JobModification callbacks are launched using low priority threads whereas the JobTransferred and the JobError callbacks are launched using higher priority threads. So it is possible that while some JobModification callbacks are pending the JobTransferred callback is received by the client first although it is launched after the pending JobModification callbacks.

BITS supports up to four simultaneous notifications per user. If one or more applications  block all four notifications for a user from returning, an application running as the same user will not receive  notifications until one or more of the blocking notifications return. To reduce the chance that your callback blocks other notifications, keep your implementation short.
			
			

If an administrator takes ownership of the job, the notification callbacks are made in the context of the user who requested notification.

If your application uses the <a href="/windows/desktop/com/single-threaded-apartments">single-threaded apartment</a> model, your callback methods can become reentrant if you call COM objects from inside your callback method. For example, if you call <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getprogress">IBackgroundCopyJob::GetProgress</a> from inside your <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-jobmodification">JobModification</a> callback, BITS can send your job modification callback another notification while you are still processing the current notification. If it is not important to your application to respond to every <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopycallback-jobmodification">JobModification</a> callback, you could ignore reentrant callbacks as shown in the following example. 


```cpp
//A member variable is used to determine if the callback
//is already processing another job modification callback.
LONG m_PendingJobModificationCount = 0;

//If you are already processing a callback, ignore this notification.
if (InterlockedCompareExchange(&m_PendingJobModificationCount, 1, 0) == 1)
{
  return S_OK;
}

...  //processing the current notification

m_PendingJobModificationCount = 0;
return hr;

```



#### Examples

The following example shows an 
<b>IBackgroundCopyCallback</b> implementation. For an example that calls this implementation, see the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> method.


```cpp
#define TWO_GB 2147483648    // 2GB


class CNotifyInterface : public IBackgroundCopyCallback
{
  LONG m_lRefCount;

public:
  //Constructor, Destructor
  CNotifyInterface() {m_lRefCount = 1;};
  ~CNotifyInterface() {};

  //IUnknown
  HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
  ULONG __stdcall AddRef();
  ULONG __stdcall Release();

  //IBackgroundCopyCallback methods
  HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
  HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
  HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);
};

HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
  if (riid == __uuidof(IUnknown) || riid == __uuidof(IBackgroundCopyCallback)) 
  {
    *ppvObj = this;
  }
  else
  {
    *ppvObj = NULL;
    return E_NOINTERFACE;
  }

  AddRef();
  return NOERROR;
}

ULONG CNotifyInterface::AddRef() 
{
  return InterlockedIncrement(&m_lRefCount);
}

ULONG CNotifyInterface::Release() 
{
  ULONG  ulCount = InterlockedDecrement(&m_lRefCount);

  if(0 == ulCount) 
  {
    delete this;
  }

  return ulCount;
}

HRESULT CNotifyInterface::JobTransferred(IBackgroundCopyJob* pJob)
{
  HRESULT hr;

  //Add logic that will not block the callback thread. If you need to perform
  //extensive logic at this time, consider creating a separate thread to perform
  //the work.

  hr = pJob->Complete();
  if (FAILED(hr))
  {
    //Handle error. BITS probably was unable to rename one or more of the 
    //temporary files. See the Remarks section of the IBackgroundCopyJob::Complete 
    //method for more details.
  }

  //If you do not return S_OK, BITS continues to call this callback.
  return S_OK;
}

HRESULT CNotifyInterface::JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError)
{
  HRESULT hr;
  BG_FILE_PROGRESS Progress;
  BG_ERROR_CONTEXT Context;
  HRESULT ErrorCode = S_OK;
  WCHAR* pszJobName = NULL;
  WCHAR* pszErrorDescription = NULL;
  BOOL IsError = TRUE;

  //Use pJob and pError to retrieve information of interest. For example,
  //if the job is an upload reply, call the IBackgroundCopyError::GetError method 
  //to determine the context in which the job failed. If the context is 
  //BG_JOB_CONTEXT_REMOTE_APPLICATION, the server application that received the 
  //upload file failed.

  hr = pError->GetError(&Context, &ErrorCode);

  //If the proxy or server does not support the Content-Range header or if
  //antivirus software removes the range requests, BITS returns BG_E_INSUFFICIENT_RANGE_SUPPORT.
  //This implementation tries to switch the job to foreground priority, so
  //the content has a better chance of being successfully downloaded.
  if (BG_E_INSUFFICIENT_RANGE_SUPPORT == ErrorCode)
  {
    hr = pError->GetFile(&pFile);
    hr = pFile->GetProgress(&Progress);
    if (BG_SIZE_UNKNOWN == Progress.BytesTotal)
    {
      //The content is dynamic, do not change priority. Handle as an error.
    }
    else if (Progress.BytesTotal > TWO_GB)
    {
      // BITS requires range requests support if the content is larger than 2 GB.
      // For these scenarios, BITS uses 2 GB ranges to download the file,
      // so switching to foreground priority will not help.

    }
    else
    {
      hr = pJob->SetPriority(BG_JOB_PRIORITY_FOREGROUND);
      hr = pJob->Resume();
      IsError = FALSE;
    }

    pFile->Release();
  }

  if (TRUE == IsError)
  {
    hr = pJob->GetDisplayName(&pszJobName);
    hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszErrorDescription);

    if (pszJobName && pszErrorDescription)
    {
      //Do something with the job name and description. 
    }

    CoTaskMemFree(pszJobName);
    CoTaskMemFree(pszErrorDescription);
  }

  //If you do not return S_OK, BITS continues to call this callback.
  return S_OK;
}

HRESULT CNotifyInterface::JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved)
{
  HRESULT hr;
  WCHAR* pszJobName = NULL;
  BG_JOB_PROGRESS Progress;
  BG_JOB_STATE State;

  hr = pJob->GetDisplayName(&pszJobName);
  if (SUCCEEDED(hr))
  {
    hr = pJob->GetProgress(&Progress);
    if (SUCCEEDED(hr))
    {
      hr = pJob->GetState(&State);
      if (SUCCEEDED(hr))
      {
        //Do something with the progress and state information.
        //BITS generates a high volume of modification
        //callbacks. Use this callback with discretion. Consider creating a timer and 
        //polling for state and progress information.
      }
    }
    CoTaskMemFree(pszJobName);
  }

  return S_OK;
}
```

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a>
