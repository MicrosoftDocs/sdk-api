---
UID: NF:shobjidl_core.IKnownFolderManager.Redirect
title: IKnownFolderManager::Redirect (shobjidl_core.h)
description: Redirects folder requests for common and per-user folders.
helpviewer_keywords: ["IKnownFolderManager interface [Windows Shell]","Redirect method","IKnownFolderManager.Redirect","IKnownFolderManager::Redirect","Redirect","Redirect method [Windows Shell]","Redirect method [Windows Shell]","IKnownFolderManager interface","_shell_IKnownFolderManager_Redirect","shell.IKnownFolderManager_Redirect","shobjidl_core/IKnownFolderManager::Redirect"]
old-location: shell\IKnownFolderManager_Redirect.htm
tech.root: shell
ms.assetid: 0f4fc609-597b-4c72-b875-4b3f051dd056
ms.date: 12/05/2018
ms.keywords: IKnownFolderManager interface [Windows Shell],Redirect method, IKnownFolderManager.Redirect, IKnownFolderManager::Redirect, Redirect, Redirect method [Windows Shell], Redirect method [Windows Shell],IKnownFolderManager interface, _shell_IKnownFolderManager_Redirect, shell.IKnownFolderManager_Redirect, shobjidl_core/IKnownFolderManager::Redirect
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnownFolderManager::Redirect
 - shobjidl_core/IKnownFolderManager::Redirect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IKnownFolderManager.Redirect
---

# IKnownFolderManager::Redirect


## -description

Redirects folder requests for common and per-user folders.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

A reference to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> of the folder to be redirected.

### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the parent window used to display copy engine progress UI dialogs when <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags">KF_REDIRECT_WITH_UI</a> is passed in the <i>flags</i> parameter. If no progress dialog is needed, this value can be <b>NULL</b>.

### -param flags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags">KF_REDIRECT_FLAGS</a></b>

The <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags">KF_REDIRECT_FLAGS</a> options for redirection.

### -param pszTargetPath [in, optional]

Type: <b>LPCWSTR</b>

A pointer to the new path for the folder. This is a null-terminated Unicode string. This value can be <b>NULL</b>.

### -param cFolders [in]

Type: <b>UINT</b>

The number of <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> values in the array at <i>pExclusion</i>.

### -param pExclusion [in]

Type: <b>KNOWNFOLDERID const*</b>

Pointer to an array of <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> values that refer to subfolders of <i>rfid</i> that should be excluded from the redirection. If no subfolders are excluded, this value can be <b>NULL</b>.

### -param ppszError [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode string that contains an error message if one was generated. This value can be <b>NULL</b>.

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

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>