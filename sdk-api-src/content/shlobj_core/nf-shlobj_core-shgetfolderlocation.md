---
UID: NF:shlobj_core.SHGetFolderLocation
title: SHGetFolderLocation function (shlobj_core.h)
description: Deprecated. Retrieves the path of a folder as an ITEMIDLIST structure.
helpviewer_keywords: ["SHGetFolderLocation","SHGetFolderLocation function [Windows Shell]","_win32_SHGetFolderLocation","shell.SHGetFolderLocation","shlobj_core/SHGetFolderLocation"]
old-location: shell\SHGetFolderLocation.htm
tech.root: shell
ms.assetid: 6fcac066-1ab0-443a-9994-b68ead3bbc20
ms.date: 12/05/2018
ms.keywords: SHGetFolderLocation, SHGetFolderLocation function [Windows Shell], _win32_SHGetFolderLocation, shell.SHGetFolderLocation, shlobj_core/SHGetFolderLocation
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetFolderLocation
 - shlobj_core/SHGetFolderLocation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHGetFolderLocation
---

# SHGetFolderLocation function


## -description

Deprecated. Retrieves the path of a folder as an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

Reserved.

### -param csidl [in]

Type: <b>int</b>

A <a href="/windows/desktop/shell/csidl">CSIDL</a> value that identifies the folder to be located. The folders associated with the CSIDLs might not exist on a particular system.

### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> that can be used to represent a particular user. It is usually set to <b>NULL</b>, but it may be needed when there are multiple users for those folders that are treated as belonging to a single user. The most commonly used folder of this type is <b>My Documents</b>. The calling application is responsible for correct impersonation when <i>hToken</i> is non-<b>NULL</b>. It must have appropriate security privileges for the particular user, and the user's registry hive must be currently mounted. See <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> for further discussion of access control issues.
    
    					

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This allows clients of <b>SHGetFolderLocation</b> to find folder locations (such as the Desktop folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as <b>My Documents</b> and <b>Desktop</b>. Any items added to the Default User folder also appear in any new user account.

### -param dwFlags [in]

Type: <b>DWORD</b>

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

The address of a pointer to an item identifier list structure that specifies the folder's location relative to the root of the namespace (the desktop). The <i>ppidl</i> parameter is set to <b>NULL</b> on failure. The calling application is responsible for freeing this resource by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/shell/csidl">CSIDL</a> in <i>nFolder</i> is valid but the folder does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/shell/csidl">CSIDL</a> in <i>nFolder</i> is not valid.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  As of Windows Vista, this function is merely a wrapper for <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a>. The CSIDL value is translated to its associated <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> and <b>SHGetKnownFolderIDList</b> is called. New applications should use the known folder system rather than the older CSIDL system, which is supported only for backward compatibility.</div>
<div> </div>
The <b>SHGetFolderLocation</b>, <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a>, <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation">SHGetSpecialFolderLocation</a>, and <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha">SHGetSpecialFolderPath</a> functions are the preferred ways to obtain handles to folders on systems earlier than Windows Vista. Functions such as <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">ExpandEnvironmentStrings</a> that use the environment variable names directly, in the form %VariableName%, may not be reliable.

This function is a superset of <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation">SHGetSpecialFolderLocation</a>, included with earlier versions of the Shell.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist">IKnownFolder::GetIDList</a>