---
UID: NF:bits.IBackgroundCopyJob.AddFileSet
title: IBackgroundCopyJob::AddFileSet
author: windows-sdk-content
description: Adds multiple files to a job.
old-location: bits\ibackgroundcopyjob_addfileset.htm
old-project: bits
ms.assetid: fe2f9b47-0f0a-48ab-be0e-658307cfec5f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddFileSet, AddFileSet method [BITS], AddFileSet method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],AddFileSet method, IBackgroundCopyJob.AddFileSet, IBackgroundCopyJob::AddFileSet, _drz_ibackgroundcopyjob_addfileset, bits.ibackgroundcopyjob_addfileset, bits/IBackgroundCopyJob::AddFileSet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.AddFileSet
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::AddFileSet


## -description


 
Adds multiple files to a job.


## -parameters




### -param cFileCount [in]

Number of elements in <i>paFileSet</i>.


### -param pFileSet






#### - paFileSet [in]

Array of 
<a href="https://msdn.microsoft.com/en-us/library/Aa362800(v=VS.85).aspx">BG_FILE_INFO</a> structures that identify the local and remote file names of the files to transfer. 




Upload jobs are restricted to a single file. If the array contains more than one element, or the job already contains a file, the method returns BG_E_TOO_MANY_FILES.


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
Files were successfully added to the job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_TOO_MANY_FILES</b></dt>
</dl>
</td>
<td width="60%">
Upload jobs can only contain one file; you cannot add more than one file to the job. None of the files in the array were added to the job.

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



It is more efficient to call the <b>AddFileSet</b> method when adding multiple files to a job than to call the <a href="https://msdn.microsoft.com/en-us/library/Aa363017(v=VS.85).aspx">IBackgroundCopyJob::AddFile</a> method in a loop. To add a single file to a job, call the 
<b>AddFile</b> method. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa362779(v=VS.85).aspx">Adding Files to a Job</a>.

To add a file to a job from which BITS downloads ranges of data from the file, call the <a href="https://msdn.microsoft.com/en-us/library/Aa362991(v=VS.85).aspx">IBackgroundCopyJob3::AddFileWithRanges</a> method.

Upload jobs can contain only one file. If you add more than one file, the method returns BG_E_TOO_MANY_FILES.

For downloads, BITS guarantees that the version of a file (based on file size and date, not content) that it transfers will be consistent; however, it does not guarantee that a set of files will be consistent. For example, if BITS is in the middle of downloading the second of two files at the time that the files are updated on the server, BITS restarts the download of the second file; however, the first file is not downloaded again.

Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file. If you use the same URL for  new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale. 

For uploads, BITS generates an error if the local file changes while the file is transferring. The error code is BG_E_FILE_CHANGED and the context is BG_ERROR_CONTEXT_LOCAL_FILE.

BITS transfers the files within a job  sequentially. If an error occurs while transferring a file, the job moves to an error state and no more files within the job are processed until the error is resolved.

By default, a user can add up to 200 files to a job. This limit does not apply to administrators or service accounts. To change the default, set the <b>MaxFilesPerJob</b> group policies.

<b>Prior to Windows Vista:  </b>There is no limit on the number of files that a user can add to a job.

For scalability concerns, see <a href="https://msdn.microsoft.com/en-us/library/Aa362783(v=VS.85).aspx">Best Practices When Using BITS</a>.


#### Examples

The following example shows how to add multiple files to a download job. The example assumes the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a> interface pointer is valid.


```cpp
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_FILE_INFO* paFiles = NULL;
int idx = 0;
int nCount = 0;  //Number of files to add to the job.
LPWSTR pszLocalName = NULL;
LPWSTR pszRemoteName = NULL;

//Set nCount to the number of files to transfer.

//Allocate a block of memory to contain the array of BG_FILE_INFO structures.
//The BG_FILE_INFO structure contains the local and remote names of the 
//file being transferred.
paFiles = (BG_FILE_INFO*) malloc(sizeof(BG_FILE_INFO) * nCount);
if (NULL == paFiles)
{
  //Handle error
}
else
{
  //Add local and remote file name pairs to the memory block. 
  for (idx=0; idx<nCount; idx++)
  {
    //Set pszLocalName to point to an LPWSTR that contains the local name or
    //allocate memory for pszLocalName and copy the local name to pszLocalName.
    (paFiles+idx)->LocalName = pszLocalName;

    //Set pszRemoteName to point to an LPWSTR that contains the remote name or
    //allocate memory for pszRemoteName and copy the remote name to pszRemoteName.
    (paFiles+idx)->RemoteName = pszRemoteName;
  }

  //Add the files to the job.
  hr = pJob->AddFileSet(nCount, paFiles);
  if (SUCCEEDED(hr))
  {
     //Do Something.
  }

  //Free the memory block for the array of BG_FILE_INFO structures. If you allocated
  //memory for the local and remote file names, loop through the array and free the
  //memory for the file names before you free paFiles.
  free(paFiles);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362991(v=VS.85).aspx">IBackgroundCopyJob3::AddFileWithRanges</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363017(v=VS.85).aspx">IBackgroundCopyJob::AddFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363022(v=VS.85).aspx">IBackgroundCopyJob::EnumFiles</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363036(v=VS.85).aspx">IBackgroundCopyJob::GetState</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363039(v=VS.85).aspx">IBackgroundCopyJob::Resume</a>
 

 

