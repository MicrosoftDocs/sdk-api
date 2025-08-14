---
UID: NF:shlobj_core.SHGetKnownFolderPath
title: SHGetKnownFolderPath function (shlobj_core.h)
description: Retrieves the full path of a known folder identified by the folder's KNOWNFOLDERID.
helpviewer_keywords: ["SHGetKnownFolderPath","SHGetKnownFolderPath function [Windows Shell]","_shell_SHGetKnownFolderPath","shell.SHGetKnownFolderPath","shlobj_core/SHGetKnownFolderPath"]
old-location: shell\SHGetKnownFolderPath.htm
tech.root: shell
ms.assetid: 5434c744-484b-4c34-9a76-dddbcb81eb29
ms.date: 12/05/2018
ms.keywords: SHGetKnownFolderPath, SHGetKnownFolderPath function [Windows Shell], _shell_SHGetKnownFolderPath, shell.SHGetKnownFolderPath, shlobj_core/SHGetKnownFolderPath
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
 - SHGetKnownFolderPath
 - shlobj_core/SHGetKnownFolderPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - Windows.Storage.dll
api_name:
 - SHGetKnownFolderPath
---

# SHGetKnownFolderPath function


## -description

Retrieves the full path of a known folder identified by the folder's <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that identifies the folder.

### -param dwFlags [in]

Type: <b>DWORD</b>

Flags that specify special retrieval options. This value can be 0; otherwise, one or more of the <a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag">KNOWN_FOLDER_FLAG</a> values.

### -param hToken [in, optional]

Type: <b>HANDLE</b>

An <a href="/windows/desktop/SecAuthZ/access-tokens">access token</a> that represents a particular user. If this parameter is <b>NULL</b>, which is the most common usage, the function requests the known folder for the current user. 
    
                        

Request a specific user's folder by passing the <i>hToken</i> of that user. This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user. That token must be opened with <a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">TOKEN_QUERY</a> and <a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">TOKEN_IMPERSONATE</a> rights. In some cases, you also need to include <a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">TOKEN_DUPLICATE</a>. In addition to passing the user's <i>hToken</i>, the registry hive of that specific user must be mounted. See <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a> for further discussion of access control issues.

Assigning the <i>hToken</i> parameter a value of -1 indicates the Default User. This allows clients of <b>SHGetKnownFolderPath</b> to find folder locations (such as the <b>Desktop</b> folder) for the Default User. The Default User user profile is duplicated when any new user account is created, and includes special folders such as <b>Documents</b> and <b>Desktop</b>. Any items added to the Default User folder also appear in any new user account. Note that access to the Default User folders requires administrator privileges.

### -param ppszPath [out]

Type: <b>PWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode string that specifies the path of the known folder. The calling process is responsible for freeing this resource once it is no longer needed by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>, whether <b>SHGetKnownFolderPath</b> succeeds or not. The returned path does not include a trailing backslash. For example, "C:\Users" is returned rather than "C:\Users\\".

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> which does not have a path (such as a folder marked as <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">KF_CATEGORY_VIRTUAL</a>).

</td>
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

This function replaces <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a>. That older function is now simply a wrapper for <b>SHGetKnownFolderPath</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath">IKnownFolder::GetPath</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist">SHGetKnownFolderIDList</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath">SHSetKnownFolderPath</a>
