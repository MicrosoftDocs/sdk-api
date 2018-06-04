---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IBackgroundCopyFile3::SetValidationState


## -description


Sets the validation state of this file.


## -parameters




### -param state






#### - State [in]

Set to <b>TRUE</b> if the file content is valid, otherwise, <b>FALSE</b>.


## -returns



The method returns the following return values.

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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
You cannot validate the file until the download is complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_RECORD_DELETED</b></dt>
</dl>
</td>
<td width="60%">
The cached record associated with this file has been deleted.

</td>
</tr>
</table>
 




## -remarks



If you set the validation state to <b>FALSE</b> and the file was downloaded from the origin server, the job moves to the error state with an error code of BG_E_VALIDATION_FAILED and the file progress is set to zero. You can then call the <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method to download the file again. 

<b>BITS 3.0:  </b>Do not call the <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method to download the file again. Instead, call the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> or <a href="https://msdn.microsoft.com/bb3f32d9-298a-4099-8d87-4057ddefb0ba">IBackgroundCopyJob::Cancel</a> method to cleanup the current job and then create a new job to download the file.

If you set the validation state to <b>FALSE</b> and the file was downloaded from a peer, BITS removes the file from the cache, resets the file progress to zero, and downloads the file again from the origin server.

You can call this method only after BITS finishes transferring the file. To receive notification when the transfer is complete, implement the <a href="https://msdn.microsoft.com/c7e22911-9c14-48ef-8283-f0787b089432">IBackgroundCopyCallback2::FileTransferred</a> method.

Calling the <a href="https://msdn.microsoft.com/d57b0b2e-1181-45ed-b7fc-d002d14527cf">IBackgroundCopyJob::Complete</a> method implicitly validates the file.

If you validate a file in the cache and then call <a href="https://msdn.microsoft.com/53daa02c-1dd2-4b9a-a52f-3a77d6cb0b2c">IBackgroundCopyJob4::SetPeerCachingFlags</a>  to disable caching (or peer caching is disable through Group Policy), the file remains in the cache. If you disable caching before validating the file, BITS removes the file from the cache.




## -see-also




<a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>



<a href="https://msdn.microsoft.com/705644e2-fd15-4225-b26a-e75c2dd2f6e3">IBackgroundCopyFile3::GetValidationState</a>



<a href="https://msdn.microsoft.com/f492f009-bef7-412e-8626-ae84cd5ce03f">IBitsPeerCacheRecord::IsFileValidated</a>
 

 

