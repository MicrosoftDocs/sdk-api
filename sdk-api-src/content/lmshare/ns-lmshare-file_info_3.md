---
UID: NS:lmshare._FILE_INFO_3
title: FILE_INFO_3 (lmshare.h)
description: Contains the identification number and other pertinent information about files, devices, and pipes.
helpviewer_keywords: ["*LPFILE_INFO_3","*PFILE_INFO_3","FILE_INFO_3","FILE_INFO_3 structure [Files]","LPFILE_INFO_3","LPFILE_INFO_3 structure pointer [Files]","PERM_FILE_CREATE","PERM_FILE_READ","PERM_FILE_WRITE","PFILE_INFO_3","PFILE_INFO_3 structure pointer [Files]","_win32_file_info_3_str","fs.file_info_3_str","lmshare/FILE_INFO_3","lmshare/LPFILE_INFO_3","lmshare/PFILE_INFO_3","netmgmt.file_info_3_str"]
old-location: fs\file_info_3_str.htm
tech.root: fs
ms.assetid: 67f5fa89-12c7-46fb-a118-de4bfed96923
ms.date: 12/05/2018
ms.keywords: '*LPFILE_INFO_3, *PFILE_INFO_3, FILE_INFO_3, FILE_INFO_3 structure [Files], LPFILE_INFO_3, LPFILE_INFO_3 structure pointer [Files], PERM_FILE_CREATE, PERM_FILE_READ, PERM_FILE_WRITE, PFILE_INFO_3, PFILE_INFO_3 structure pointer [Files], _win32_file_info_3_str, fs.file_info_3_str, lmshare/FILE_INFO_3, lmshare/LPFILE_INFO_3, lmshare/PFILE_INFO_3, netmgmt.file_info_3_str'
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FILE_INFO_3, *PFILE_INFO_3, *LPFILE_INFO_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_INFO_3
 - lmshare/_FILE_INFO_3
 - PFILE_INFO_3
 - lmshare/PFILE_INFO_3
 - FILE_INFO_3
 - lmshare/FILE_INFO_3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmshare.h
api_name:
 - FILE_INFO_3
---

# FILE_INFO_3 structure


## -description

Contains the identification number and other pertinent information about files, devices, and pipes.

## -struct-fields

### -field fi3_id

Specifies a DWORD value that contains the identification number assigned to the resource when it is opened.

### -field fi3_permissions

Specifies a DWORD value that contains the access permissions associated with the opening application. This member can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PERM_FILE_READ"></a><a id="perm_file_read"></a><dl>
<dt><b>PERM_FILE_READ</b></dt>
</dl>
</td>
<td width="60%">
Permission to read a resource and, by default, execute the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="PERM_FILE_WRITE"></a><a id="perm_file_write"></a><dl>
<dt><b>PERM_FILE_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Permission to write to a resource.

</td>
</tr>
<tr>
<td width="40%"><a id="PERM_FILE_CREATE"></a><a id="perm_file_create"></a><dl>
<dt><b>PERM_FILE_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Permission to create a resource; data can be written when creating the resource.

</td>
</tr>
</table>

### -field fi3_num_locks

Specifies a DWORD value that contains the number of file locks on the file, device, or pipe.

### -field fi3_pathname

Pointer to a string that specifies the path of the opened resource.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field fi3_username

Pointer to a string that specifies which user (on servers that have user-level security) or which computer (on servers that have share-level security) opened the resource. Note that Windows does not support share-level security.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

## -see-also

<a href="/windows/desktop/api/lmshare/ns-lmshare-file_info_2">FILE_INFO_2</a>



<a href="/windows/desktop/NetShare/netfile-functions">NetFile Functions</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netfileenum">NetFileEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo">NetFileGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>