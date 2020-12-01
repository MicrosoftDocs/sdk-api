---
UID: NF:shlobj_core.SHGetKnownFolderIDList
title: SHGetKnownFolderIDList function (shlobj_core.h)
description: Retrieves the path of a known folder as an ITEMIDLIST structure.
helpviewer_keywords: ["SHGetKnownFolderIDList","SHGetKnownFolderIDList function [Windows Shell]","_shell_SHGetKnownFolderIDList","shell.SHGetKnownFolderIDList","shlobj_core/SHGetKnownFolderIDList"]
old-location: shell\SHGetKnownFolderIDList.htm
tech.root: shell
ms.assetid: fed9cfb8-4c38-4947-99aa-278245148136
ms.date: 12/05/2018
ms.keywords: SHGetKnownFolderIDList, SHGetKnownFolderIDList function [Windows Shell], _shell_SHGetKnownFolderIDList, shell.SHGetKnownFolderIDList, shlobj_core/SHGetKnownFolderIDList
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetKnownFolderIDList
 - shlobj_core/SHGetKnownFolderIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - SHGetKnownFolderIDList
---

# SHGetKnownFolderIDList function


## -description

Retrieves the path of a known folder as an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that identifies the folder. The folders associated with the known folder IDs might not exist on a particular system.

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, it is one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a> values.

### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> used to represent a particular user. This parameter is usually set to <b>NULL</b>, in which case the function tries to access the current user's instance of the folder. However, you may need to assign a value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <b>Documents</b>.

The calling application is responsible for correct impersonation when <i>hToken</i> is non-null. It must have appropriate security privileges for the particular user, including TOKEN_QUERY and TOKEN_IMPERSONATE, and the user's registry hive must be currently mounted. See <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> for further discussion of access control issues.

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This allows clients of <b>SHGetKnownFolderIDList</b> to find folder locations (such as the <b>Desktop</b> folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as <b>Documents</b> and <b>Desktop</b>. Any items added to the Default User folder also appear in any new user account. Note that access to the Default User folders requires administrator privileges.

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns, contains a pointer to the PIDL of the folder. This parameter is passed uninitialized. The caller is responsible for freeing the returned PIDL when it is no longer needed by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree">ILFree</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that is not present on the system. Not all <b>KNOWNFOLDERID</b> values are present on all systems. Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids">IKnownFolderManager::GetFolderIds</a> to retrieve the set of <b>KNOWNFOLDERID</b> values for the current system.

</td>
</tr>
</table>

## -remarks

This function replaces <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation">SHGetFolderLocation</a>. That older function is now simply a wrapper for <b>SHGetKnownFolderIDList</b>.

Callers using this function must have at least User privileges.

Some known folders, for example, the <b>Documents</b> folder, are per-user. Each user has a different path for the <b>Documents</b> folder. If <i>hToken</i> is <b>NULL</b>, the API tries to access the current user's instance of the folder. If <i>hToken</i> is a valid user token, the API tries to impersonate the user using this token, and attempts to access that user's instance of the folder.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath">IKnownFolder::GetPath</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath">SHSetKnownFolderPath</a>