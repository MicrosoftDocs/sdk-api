---
UID: NF:bits2_0.IBackgroundCopyFile2.SetRemoteName
title: IBackgroundCopyFile2::SetRemoteName (bits2_0.h)
description: Changes the remote name to a new URL in a download job.
helpviewer_keywords: ["IBackgroundCopyFile2 interface [BITS]","SetRemoteName method","IBackgroundCopyFile2.SetRemoteName","IBackgroundCopyFile2::SetRemoteName","SetRemoteName","SetRemoteName method [BITS]","SetRemoteName method [BITS]","IBackgroundCopyFile2 interface","bits.ibackgroundcopyfile2_setremotename","bits2_0/IBackgroundCopyFile2::SetRemoteName"]
old-location: bits\ibackgroundcopyfile2_setremotename.htm
tech.root: Bits
ms.assetid: 6dd33b7d-4317-4eb5-aae4-83d3f4416bf9
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile2 interface [BITS],SetRemoteName method, IBackgroundCopyFile2.SetRemoteName, IBackgroundCopyFile2::SetRemoteName, SetRemoteName, SetRemoteName method [BITS], SetRemoteName method [BITS],IBackgroundCopyFile2 interface, bits.ibackgroundcopyfile2_setremotename, bits2_0/IBackgroundCopyFile2::SetRemoteName
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003,  and Windows XP
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile2::SetRemoteName
 - bits2_0/IBackgroundCopyFile2::SetRemoteName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyFile2.SetRemoteName
---

# IBackgroundCopyFile2::SetRemoteName


## -description

Changes the remote name to a new URL in a download job.

## -parameters

### -param Val [in]

Null-terminated string that contains the name of the file on the server. For information on specifying the remote name, see the <b>RemoteName</b> member and Remarks section of the <a href="/windows/desktop/api/bits/ns-bits-bg_file_info">BG_FILE_INFO</a> structure.

## -returns

This method returns the following return values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
You cannot call this method for upload or upload-reply jobs; only call this method for download jobs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be <b>BG_JOB_STATE_CANCELLED</b> or <b>BG_JOB_STATE_ACKNOWLEDGED</b>.

</td>
</tr>
</table>

## -remarks

 Typically, you call this method if you want to change the protocol used to transfer the file (for example, from SMB to HTTP) or if you want to change the file name or path.

This method does not serialize when it returns. To serialize the change, <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-suspend">suspend</a> the job, call this method (if changing multiple files in the job, use a loop), and <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">resume</a> the job. Calling the <b>IBackgroundCopyJob::Resume</b> method serializes the change. 

If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), BITS restarts the download. Otherwise, the transfer resumes from the same position on the new server. BITS does not restart already transferred files. 

If the remote name identifies a server message block (SMB) path, the following table identifies possible error codes that can occur after you resume the job. These errors place the job in the <b>BG_JOB_STATE_ERROR</b> state.

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td><code>HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND)</code></td>
<td> The directory was not found. </td>
</tr>
<tr>
<td><code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code></td>
<td>The file was not found.</td>
</tr>
<tr>
<td><code>HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</code></td>
<td>The user does not have access to the file specified in <i>Val</i>.</td>
</tr>
</table>
 


#### Examples

The following example shows how to call the <b>SetRemoteName</b> method to change the remote name of a file. The example assumes the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> variable, pJob, is valid and the job contains one or more files.


```cpp
     IBackgroundCopyJob *pJob;
     IEnumBackgroundCopyFiles* pFiles = NULL;
     IBackgroundCopyFile* pFile = NULL;
     IBackgroundCopyFile2* pFile2 = NULL;
     WCHAR* pRemoteFileName = NULL;
     ULONG cFileCount = 0;

     hr = pJob->Suspend();
     hr = pJob->EnumFiles(&pFiles);
     if (SUCCEEDED(hr))
     {
          //Get the count of files in the job. 
          hr = pFiles->GetCount(&cFileCount);

          //Enumerate the files in the job.
          for (ULONG idx=0; idx<cFileCount; idx++)
          {
               hr = pFiles->Next(1, &pFile, NULL);
               if (S_OK == hr)
               {
                    //Get the local name of the file.
                    hr = pFile->GetRemoteName(&pRemoteFileName);
                    if (SUCCEEDED(hr))
                    {
                         //Determine if you want to replace the remote name of this file.
                         if (<CONDITIONGOESHERE>)
                         {
                              //Need to query the IBackgroundCopyFile interface for an IBackgroundCopyFile2
                              //interface pointer. The IBackgroundCopyFile2 interface contains the SetRemoteName method.
                              hr = pFile->QueryInterface(__uuidof(IBackgroundCopyFile2), (void**)&pFile2);
                              if (S_OK == hr)
                              {
                                   hr = pFile2->SetRemoteName(L"<NEWURLGOESHERE>");
                                   if (FAILED(hr))
                                   {
                                        //Handle error. 
                                        //Returns E_NOTIMPL if not a download job.
                                        //Returns E_INVALIDARG if invalid URL.
                                   }
                              }
                              else
                              {
                                   //handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
                                   //running on the computer is less than BITS 2.0.
                              }
                         }
                         CoTaskMemFree(pRemoteFileName); 
                    }    
                    pFile->Release(); 
                    pFile = NULL;
               }
               else
               {
                    //Handle error
                    break;
               }
          }

          pFiles->Release();
          pFiles = NULL;
     }

     hr = pJob->Resume(); //Force the job to serialize.


```

## -see-also

<a href="/windows/desktop/api/bits2_0/nn-bits2_0-ibackgroundcopyfile2">IBackgroundCopyFile2</a>



<a href="/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix">IBackgroundCopyJob3::ReplaceRemotePrefix</a>