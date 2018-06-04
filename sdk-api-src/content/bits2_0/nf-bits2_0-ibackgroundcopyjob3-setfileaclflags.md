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

# IBackgroundCopyJob3::SetFileACLFlags


## -description


Specifies the owner and ACL information to maintain when using SMB to download or upload a file.


## -parameters




### -param Flags [in]

Flags that identify the owner and ACL information to maintain when transferring a file using SMB. Subsequent calls to this method overwrite the previous flags. Specify 0 to remove the flags from the job. You can specify any combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_OWNER"></a><a id="bg_copy_file_owner"></a><dl>
<dt><b>BG_COPY_FILE_OWNER</b></dt>
</dl>
</td>
<td width="60%">
If set, the file's owner information is maintained. Otherwise, the user who calls the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406719">Complete</a> method owns the file.

You must have SeRestorePrivilege to set this flag. The administrators group contains the SeRestorePrivilege privilege.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_GROUP"></a><a id="bg_copy_file_group"></a><dl>
<dt><b>BG_COPY_FILE_GROUP</b></dt>
</dl>
</td>
<td width="60%">
If set, the file's group information is maintained. Otherwise, BITS uses the job owner's primary group to assign the group information to the file.

You must have SeRestorePrivilege to set this flag. The administrators group contains the SeRestorePrivilege privilege.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_DACL"></a><a id="bg_copy_file_dacl"></a><dl>
<dt><b>BG_COPY_FILE_DACL</b></dt>
</dl>
</td>
<td width="60%">
If set, BITS copies the explicit ACEs from the source file and inheritable  ACEs from the destination  folder.
Otherwise, BITS copies the inheritable ACEs from the destination  folder. If the destination folder does not contain inheritable ACEs, BITS uses the default DACL from the owner's account.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_SACL"></a><a id="bg_copy_file_sacl"></a><dl>
<dt><b>BG_COPY_FILE_SACL</b></dt>
</dl>
</td>
<td width="60%">
If set, BITS copies the explicit ACEs from the source file and inheritable  ACEs from the destination  folder.
Otherwise, BITS copies the inheritable ACEs from the destination  folder.

You must have SeSecurityPrivilege on both the local and remote computers to set this flag. The administrators group contains the SeSecurityPrivilege privilege.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_ALL"></a><a id="bg_copy_file_all"></a><dl>
<dt><b>BG_COPY_FILE_ALL</b></dt>
</dl>
</td>
<td width="60%">
If set, BITS copies the owner and ACL information. This is the same as setting all the flags individually.

</td>
</tr>
</table>
 


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
Successfully set the flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
You must call this method before the job transitions to the <a href="https://msdn.microsoft.com/a7857cf1-05b7-42df-b79e-50a2f6a406dc">BG_JOB_STATE_TRANSFERRED</a> state. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Flags</i> parameter contains a flag that is not in the list.

</td>
</tr>
</table>
 




## -remarks



These flags apply to remote file names that specify the SMB protocol. BITS ignores the flags for HTTP transfers.

BITS propagates the file time stamps and  attributes (not extended attributes) for SMB files. 

BITS applies the owner and ACL information to the file at the time the file transfer is complete, not when it <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">creates</a> the temporary transfer file. BITS does not specify a security descriptor when it creates the temporary transfer file (the file inherits the ACL information from the destination directory). If the transferred data is sensitive, the application should specify an appropriate ACL on the destination directory to prevent unauthorized access.

To ensure the proper owner and ACL information is set on all files in the job, call this method after you create the job and before calling the <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method. Otherwise, those files that transferred before the flags were set will not contain the appropriate owner and ACL information. 

This method is modeled after the XCopy DOS command.

The owner and ACL information is not maintained if you download to a FAT file system.

If the user does not have privileges on the local and remote computers to copy the owner or ACL information, BITS places the job in a transient error state and sets the error code to <b>E_ACCESSDENIED</b>.


#### Examples

The following example shows how to call the <b>SetFileACLFlags</b> method to specify what owner and ACL information to maintain with the files that BITS downloads. The example assumes the <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> variable, pJob, is valid, points to a new job, and is suspended.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>     IBackgroundCopyJob *pJob;
     IBackgroundCopyJob3 *pJob3 = NULL;

     //Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob3
     //interface pointer. The IBackgroundCopyJob3 interface contains the SetACLFlags method.
     hr = pJob-&gt;QueryInterface(__uuidof( IBackgroundCopyJob3 ), (void**)&amp;pJob3;);
     if (S_OK == hr)
     {
          pJob-&gt;Release(); //No longer need the IBackgoundCopyJob interface pointer.

          //Copy the group and DACL information for each file.
          hr = pJob3-&gt;SetACLFlags(BG_COPY_FILE_GROUP | BG_COPY_FILE_DACL);
          if (FAILED(hr))
          {
               //Handle error.
          }

          ... //Add one or more files and resume the job.
          pJob3-&gt;Resume();

          //When done, release the interface pointer.
          pJob3-&gt;Release();
     }
     else
     {
          //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
          //running on the computer is less than BITS 2.0.
     }</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>



<a href="https://msdn.microsoft.com/569df1e5-d45a-4f18-82ad-1e4957f47d94">IBackgroundCopyJob3::GetFileACLFlags</a>
 

 

