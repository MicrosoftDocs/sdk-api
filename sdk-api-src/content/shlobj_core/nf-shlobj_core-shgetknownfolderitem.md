---
UID: NF:shlobj_core.SHGetKnownFolderItem
title: SHGetKnownFolderItem function (shlobj_core.h)
description: Retrieves an IShellItem object that represents a known folder.
helpviewer_keywords: ["SHGetKnownFolderItem","SHGetKnownFolderItem function [Windows Shell]","_shell_SHGetKnownFolderItem","shell.SHGetKnownFolderItem","shlobj_core/SHGetKnownFolderItem"]
old-location: shell\SHGetKnownFolderItem.htm
tech.root: shell
ms.assetid: d0880a8c-20dd-47cc-b6c5-23dedb32d453
ms.date: 12/05/2018
ms.keywords: SHGetKnownFolderItem, SHGetKnownFolderItem function [Windows Shell], _shell_SHGetKnownFolderItem, shell.SHGetKnownFolderItem, shlobj_core/SHGetKnownFolderItem
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetKnownFolderItem
 - shlobj_core/SHGetKnownFolderItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
 - Windows.Storage.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHGetKnownFolderItem
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHGetKnownFolderItem function


## -description

Retrieves an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents a known folder.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>, a <b>GUID</b> that identifies the folder that contains the item.

### -param flags [in]

Type: <b><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a></b>

Flags that specify special options used in the retrieval of the known folder <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>. This value can be <b>KF_FLAG_DEFAULT</b>; otherwise, one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a> values.

### -param hToken [in]

Type: <b>HANDLE</b>

An <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> used to represent a particular user. This parameter is usually set to <b>NULL</b>, in which case the function tries to access the current user's instance of the folder. However, you may need to assign a value to <i>hToken</i> for those folders that can have multiple users but are treated as belonging to a single user. The most commonly used folder of this type is <b>Documents</b>.



The calling application is responsible for correct impersonation when <i>hToken</i> is non-<b>null</b>. It must have appropriate security privileges for the particular user, including TOKEN_QUERY and TOKEN_IMPERSONATE, and the user's registry hive must be currently mounted. See <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> for further discussion of access control issues.

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This allows clients of <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath">SHSetKnownFolderPath</a> to set folder locations (such as the <b>Desktop</b> folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as <b>Documents</b> and <b>Desktop</b>. Any items added to the Default User folder also appear in any new user account. Note that access to the Default User folders requires administrator privileges.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface that represents the item, usually IID_IShellItem or IID_IShellItem2.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.

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

The caller of this function must have Administrator privileges. To call this function on public known folders, the caller must have Administrator privileges. For per-user known folders the caller only requires User privileges.

Some of the known folders, for example, the <b>Documents</b> folder, are per-user. Every user has a different path for their <b>Documents</b> folder. If <i>hToken</i> is <b>NULL</b>, the API tries to access the calling application's instance of the folder, which is that of the current user. If <i>hToken</i> is a valid user token, the API tries to impersonate the user using this token and tries to access that user's instance.

This function cannot be called on folders of type <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_FIXED</a> and <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_VIRTUAL</a>.

To call this function on a folder of type <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_COMMON</a>, the calling application must be running with elevated privileges.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath">IKnownFolder::GetPath</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect">IKnownFolderManager::Redirect</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder">SHCreateItemInKnownFolder</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a>
