---
UID: NN:bits3_0.IBackgroundCopyCallback2
title: IBackgroundCopyCallback2 (bits3_0.h)
description: Implement this interface to receive notification that a file has completed downloading.
helpviewer_keywords: ["IBackgroundCopyCallback2","IBackgroundCopyCallback2 interface [BITS]","IBackgroundCopyCallback2 interface [BITS]","described","bits.ibackgroundcopycallback2","bits3_0/IBackgroundCopyCallback2"]
old-location: bits\ibackgroundcopycallback2.htm
tech.root: Bits
ms.assetid: 9bbc323c-0caf-46a9-ba25-e72a2c6ae363
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback2, IBackgroundCopyCallback2 interface [BITS], IBackgroundCopyCallback2 interface [BITS],described, bits.ibackgroundcopycallback2, bits3_0/IBackgroundCopyCallback2
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback2
 - bits3_0/IBackgroundCopyCallback2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyCallback2
---

# IBackgroundCopyCallback2 interface


## -description

Implement this interface to 
<a href="/windows/desktop/Bits/registering-a-com-callback">receive notification</a> that a file has completed downloading. Instead of  polling for the download status of a file, clients use this interface.
			

To receive notifications, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a> method to specify the interface pointer to your 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> implementation. To specify which notifications you want to receive, call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a> method.

You must implement all methods of this interface and the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface. For example, if you do not register for the file transferred callback, your <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">FileTransferred</a> method must still return <b>S_OK</b>. If you do not want to receive the file transferred callback, you can simply implement the <b>IBackgroundCopyCallback</b> instead.

## -inheritance

The <b>IBackgroundCopyCallback2</b> interface inherits from <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>. <b>IBackgroundCopyCallback2</b> also has these types of members:

## -remarks

For more details on implementing this interface, see the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a> interface.


#### Examples

The following example shows an 
<b>IBackgroundCopyCallback2</b> implementation. This example also shows how to handle reentrant calls in the <b>JobModification</b> callback for a single-threaded apartment model.


```cpp
#define TWO_GB 2147483648    // 2GB


class CNotifyInterface : public IBackgroundCopyCallback2
{
  LONG m_lRefCount;
  LONG m_PendingJobModificationCount;

public:
  //Constructor, Destructor
  CNotifyInterface() {m_lRefCount = 1; m_PendingJobModificationCount = 0;};
  ~CNotifyInterface() {};

  //IUnknown
  HRESULT __stdcall QueryInterface(REFIID riid, LPVOID *ppvObj);
  ULONG __stdcall AddRef();
  ULONG __stdcall Release();

  //IBackgroundCopyCallback methods
  HRESULT __stdcall JobTransferred(IBackgroundCopyJob* pJob);
  HRESULT __stdcall JobError(IBackgroundCopyJob* pJob, IBackgroundCopyError* pError);
  HRESULT __stdcall JobModification(IBackgroundCopyJob* pJob, DWORD dwReserved);
  HRESULT __stdcall FileTransferred(IBackgroundCopyJob* pJob, IBackgroundCopyFile* pFile);
};

HRESULT CNotifyInterface::QueryInterface(REFIID riid, LPVOID* ppvObj) 
{
  if (riid == __uuidof(IUnknown) || 
      riid == __uuidof(IBackgroundCopyCallback) ||
      riid == __uuidof(IBackgroundCopyCallback2)) 
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
      //BITS does not use range requests if the content is less than 2 GB. 
      //However, if the content is greater than 2 GB, BITS
      //uses 2 GB ranges to download the file, so switching to foreground 
      //priority will not help.
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

  //If you are already processing a callback, ignore this notification.
  if (InterlockedCompareExchange(&m_PendingJobModificationCount, 1, 0) == 1)
  {
    return S_OK;
  }

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

  m_PendingJobModificationCount = 0;

  return S_OK;
}

HRESULT CNotifyInterface::FileTransferred(IBackgroundCopyJob* pJob, IBackgroundCopyFile* pFile)
{
  HRESULT hr = S_OK;
  IBackgroundCopyFile3* pFile3 = NULL;
  BOOL IsValid = FALSE;

  hr = pFile->QueryInterface(__uuidof(IBackgroundCopyFile3), (void**)&pFile3);
  if (SUCCEEDED(hr))
  {
    // Add code to validate downloaded content and set IsValid.

    hr = pFile3->SetValidationState(IsValid);
    if (FAILED(hr))
    {
      // Handle error
    }

    pFile3->Release();
  }

	return S_OK;
}
```

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopycallback">IBackgroundCopyCallback</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyflags">IBackgroundCopyJob::SetNotifyFlags</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnotifyinterface">IBackgroundCopyJob::SetNotifyInterface</a>
