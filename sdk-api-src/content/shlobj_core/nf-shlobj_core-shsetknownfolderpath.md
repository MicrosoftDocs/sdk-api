---
UID: NF:shlobj_core.SHSetKnownFolderPath
title: SHSetKnownFolderPath function (shlobj_core.h)
description: Redirects a known folder to a new location.
helpviewer_keywords: ["KF_FLAG_DONT_UNEXPAND","SHSetKnownFolderPath","SHSetKnownFolderPath function [Windows Shell]","_shell_SHSetKnownFolderPath","shell.SHSetKnownFolderPath","shlobj_core/SHSetKnownFolderPath"]
old-location: shell\SHSetKnownFolderPath.htm
tech.root: shell
ms.assetid: b5758086-93d1-49d6-b9ac-ba8927f3bd1e
ms.date: 12/05/2018
ms.keywords: KF_FLAG_DONT_UNEXPAND, SHSetKnownFolderPath, SHSetKnownFolderPath function [Windows Shell], _shell_SHSetKnownFolderPath, shell.SHSetKnownFolderPath, shlobj_core/SHSetKnownFolderPath
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
req.lib: 
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSetKnownFolderPath
 - shlobj_core/SHSetKnownFolderPath
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
 - SHSetKnownFolderPath
---

# SHSetKnownFolderPath function


## -description

Redirects a known folder to a new location.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A <b>GUID</b> that identifies the known folder.

### -param dwFlags [in]

Type: <b>DWORD</b>

Either 0 or the following value.



#### KF_FLAG_DONT_UNEXPAND

If this flag is set, portions of the path referenced by <i>pszPath</i> may be represented by environment strings such as <code>%USERPROFILE%</code>.

### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> used to represent a particular user. This parameter is usually set to <b>NULL</b>, in which case the function tries to access the current user's instance of the folder. However, you may need to assign a value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <b>Documents</b>.
			
            		

The calling application is responsible for correct impersonation when <i>hToken</i> is non-null. It must have appropriate security privileges for the particular user, including TOKEN_QUERY and TOKEN_IMPERSONATE, and the user's registry hive must be currently mounted. See <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> for further discussion of access control issues.

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This allows clients of <b>SHSetKnownFolderPath</b> to set folder locations (such as the <b>Desktop</b> folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as <b>Documents</b> and <b>Desktop</b>. Any items added to the Default User folder also appear in any new user account. Note that access to the Default User folders requires administrator privileges.

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to the folder's new path. This is a null-terminated Unicode string of length MAX_PATH. This path cannot be of zero length.

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

This function replaces <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha">SHSetFolderPath</a>. That older function is now simply a wrapper for <b>SHSetKnownFolderPath</b>.

The caller of this function must have Administrator privileges. To call this function on public known folders, the caller must have Administrator privileges. For per-user known folders the caller only requires User privileges.

Some of the known folders, for example, the <b>Documents</b> folder, are per-user. Every user has a different path for their <b>Documents</b> folder. If <i>hToken</i> is <b>NULL</b>, the API tries to access the calling application's instance of the folder, which is that of the current user. If <i>hToken</i> is a valid user token, the API tries to impersonate the user using this token and tries to access that user's instance.

This function cannot be called on folders of type <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_FIXED</a> and <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_VIRTUAL</a>.

To call this function on a folder of type <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_COMMON</a>, the calling application must be running with elevated privileges.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath">IKnownFolder::GetPath</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath">IKnownFolder::SetPath</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect">IKnownFolderManager::Redirect</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a>