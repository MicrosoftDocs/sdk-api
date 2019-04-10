---
UID: NF:bits.IBackgroundCopyJob.AddFile
title: IBackgroundCopyJob::AddFile (bits.h)
author: windows-sdk-content
description: Adds a single file to the job.
old-location: bits\ibackgroundcopyjob_addfile.htm
tech.root: Bits
ms.assetid: 0dada1d3-49b6-41af-b17f-612f27ea4d56
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddFile, AddFile method [BITS], AddFile method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],AddFile method, IBackgroundCopyJob.AddFile, IBackgroundCopyJob::AddFile, _drz_ibackgroundcopyjob_addfile, bits.ibackgroundcopyjob_addfile, bits/IBackgroundCopyJob::AddFile
ms.topic: method
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
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.AddFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob::AddFile


## -description


 
Adds a single file to the job.


## -parameters




### -param RemoteUrl [in]

Null-terminated string that contains the name of the file on the server. For information on specifying the remote name, see the <b>RemoteName</b> member and Remarks section of the <a href="https://msdn.microsoft.com/bf5302e9-da8f-4c57-a998-fd49484e0584">BG_FILE_INFO</a> structure.


### -param LocalName [in]

Null-terminated string that contains the name of the file on the client. For information on specifying the local name, see the <b>LocalName</b> member and Remarks section of the <a href="https://msdn.microsoft.com/bf5302e9-da8f-4c57-a998-fd49484e0584">BG_FILE_INFO</a> structure.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
File was successfully added to the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_TOO_MANY_FILES</b></dt>
</dl>
</td>
<td width="60%">
Upload jobs can only contain one file; you cannot add another file to the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_TOO_MANY_FILES_IN_JOB</b></dt>
</dl>
</td>
<td width="60%">
The MaxFilesPerJob Group Policy setting determines how many files a job can contain. Adding the file to the job exceeds the MaxFilesPerJob limit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
You can receive this error for one of the following reasons:

<ul>
<li>The local or remote file name is not valid.</li>
<li>The remote file name uses an unsupported protocol.</li>
<li>The local file name was specified using a relative path.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
User does not have permission to write to the specified directory on the client.

</td>
</tr>
</table>
 




## -remarks



To add more than one file at a time to a  job, call the 
<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">IBackgroundCopyJob::AddFileSet</a> method. It is more efficient to call the <b>AddFileSet</b> method when adding multiple files to a job than to call the <b>AddFile</b> method in a loop. For more information, see <a href="https://msdn.microsoft.com/fb6e7219-b6ca-4f72-b7a3-60d65e8f3892">Adding Files to a Job</a>.

To add a file to a job from which BITS downloads ranges of data from the file, call the <a href="https://msdn.microsoft.com/b3601f23-1a69-47db-8943-7515652cf015">IBackgroundCopyJob3::AddFileWithRanges</a> method.

Upload jobs can only contain one file. If you add a second file, the method returns BG_E_TOO_MANY_FILES.

For downloads, BITS guarantees that the version of a file (based on file size and date, not content) that it transfers will be consistent; however, it does not guarantee that a set of files will be consistent. For example, if BITS is in the middle of downloading the second of two files in the job at the time that the files are updated on the server, BITS restarts the download of the second file; however, the first file is not downloaded again.

Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file. If you use the same URL for  new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale. 

For uploads, BITS generates an error if the local file changes while the file is transferring. The error code is BG_E_FILE_CHANGED and the context is BG_ERROR_CONTEXT_LOCAL_FILE.

BITS transfers the files within a job  sequentially. If an error occurs while transferring a file, the job moves to an error state and no more files within the job are processed until the error is resolved.

By default, a user can add up to 200 files to a job. This limit does not apply to administrators or service accounts. To change the default, set the <b>MaxFilesPerJob</b> group policies.

<b>Prior to Windows Vista:  </b>There is no limit on the number of files that a user can add to a job.

For scalability concerns, see <a href="https://msdn.microsoft.com/f4a09a80-2a85-4b59-b0fd-c23c128973f7">Best Practices When Using BITS</a>.


#### Examples

For an example that adds a single file to a job, see 
<a href="https://msdn.microsoft.com/fb6e7219-b6ca-4f72-b7a3-60d65e8f3892">Adding Files to a Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b3601f23-1a69-47db-8943-7515652cf015">IBackgroundCopyJob3::AddFileWithRanges</a>



<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">IBackgroundCopyJob::AddFileSet</a>



<a href="https://msdn.microsoft.com/c6b8ef69-9c67-447f-9f90-b6905a5a5a19">IBackgroundCopyJob::EnumFiles</a>



<a href="https://msdn.microsoft.com/32789bd2-2368-473b-accf-ac6e317d0172">IBackgroundCopyJob::GetState</a>



<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a>
 

 

