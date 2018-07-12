---
UID: NF:bits2_0.IBackgroundCopyJob3.GetFileACLFlags
title: IBackgroundCopyJob3::GetFileACLFlags
author: windows-sdk-content
description: Retrieves the flags that identify the owner and ACL information to maintain when transferring a file using SMB.
old-location: bits\ibackgroundcopyjob3_getfileaclflags.htm
old-project: bits
ms.assetid: 569df1e5-d45a-4f18-82ad-1e4957f47d94
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: BG_COPY_FILE_ALL, BG_COPY_FILE_DACL, BG_COPY_FILE_GROUP, BG_COPY_FILE_OWNER, BG_COPY_FILE_SACL, GetFileACLFlags, GetFileACLFlags method [BITS], GetFileACLFlags method [BITS],IBackgroundCopyJob3 interface, IBackgroundCopyJob3 interface [BITS],GetFileACLFlags method, IBackgroundCopyJob3.GetFileACLFlags, IBackgroundCopyJob3::GetFileACLFlags, bits.ibackgroundcopyjob3_getfileaclflags, bits2_0/IBackgroundCopyJob3::GetFileACLFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003, and  Windows XP
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
tech.root: 
req.typenames: BG_AUTH_CREDENTIALS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyJob3.GetFileACLFlags
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: BitsPrx3.dll
req.irql: 
---

# IBackgroundCopyJob3::GetFileACLFlags


## -description


Retrieves the flags that identify the owner and ACL information to maintain when transferring a file using SMB.


## -parameters




### -param Flags [out]

Flags that identify the owner and ACL information to maintain when transferring a file using SMB. <i>Flags</i> can contain any combination of the following flags. If no flags are set, <i>Flags</i> is zero.

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
If set, the file's owner information is maintained. Otherwise, the job's owner becomes the  owner of the file. 

</td>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_GROUP"></a><a id="bg_copy_file_group"></a><dl>
<dt><b>BG_COPY_FILE_GROUP</b></dt>
</dl>
</td>
<td width="60%">
If set, the file's group information is maintained. Otherwise, BITS uses the job owner's primary group to assign the group information to the file.   

</td>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_DACL"></a><a id="bg_copy_file_dacl"></a><dl>
<dt><b>BG_COPY_FILE_DACL</b></dt>
</dl>
</td>
<td width="60%">
If set, BITS copies the explicit ACEs from the source file and inheritable  ACEs from the destination parent folder.
Otherwise, BITS copies the inheritable ACEs from the destination parent folder. If the parent folder does not contain inheritable ACEs, BITS uses the default DACL from the account. 

</td>
</tr>
<tr>
<td width="40%"><a id="BG_COPY_FILE_SACL"></a><a id="bg_copy_file_sacl"></a><dl>
<dt><b>BG_COPY_FILE_SACL</b></dt>
</dl>
</td>
<td width="60%">
If set, BITS copies the explicit ACEs from the source file and inheritable  ACEs from the destination parent folder.
Otherwise, BITS copies the inheritable ACEs from the destination parent folder.  

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
Successfully retrieved the flags.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>



<a href="https://msdn.microsoft.com/de218e3d-8c42-4cf3-94b9-94dbc5edbb47">IBackgroundCopyJob3::SetFileACLFlags</a>
 

 

