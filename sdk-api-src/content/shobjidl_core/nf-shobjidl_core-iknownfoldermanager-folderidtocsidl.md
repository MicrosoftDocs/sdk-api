---
UID: NF:shobjidl_core.IKnownFolderManager.FolderIdToCsidl
title: IKnownFolderManager::FolderIdToCsidl (shobjidl_core.h)
description: Gets the legacy CSIDL value that is the equivalent of a given KNOWNFOLDERID.
helpviewer_keywords: ["FolderIdToCsidl","FolderIdToCsidl method [Windows Shell]","FolderIdToCsidl method [Windows Shell]","IKnownFolderManager interface","IKnownFolderManager interface [Windows Shell]","FolderIdToCsidl method","IKnownFolderManager.FolderIdToCsidl","IKnownFolderManager::FolderIdToCsidl","_shell_IKnownFolderManager_FolderIdToCsidl","shell.IKnownFolderManager_FolderIdToCsidl","shobjidl_core/IKnownFolderManager::FolderIdToCsidl"]
old-location: shell\IKnownFolderManager_FolderIdToCsidl.htm
tech.root: shell
ms.assetid: 27bd8c79-34ff-44ee-ad99-aa079af7da89
ms.date: 12/05/2018
ms.keywords: FolderIdToCsidl, FolderIdToCsidl method [Windows Shell], FolderIdToCsidl method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FolderIdToCsidl method, IKnownFolderManager.FolderIdToCsidl, IKnownFolderManager::FolderIdToCsidl, _shell_IKnownFolderManager_FolderIdToCsidl, shell.IKnownFolderManager_FolderIdToCsidl, shobjidl_core/IKnownFolderManager::FolderIdToCsidl
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnownFolderManager::FolderIdToCsidl
 - shobjidl_core/IKnownFolderManager::FolderIdToCsidl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolderManager.FolderIdToCsidl
---

# IKnownFolderManager::FolderIdToCsidl


## -description

Gets the legacy <a href="/windows/desktop/shell/csidl">CSIDL</a> value that is the equivalent of a given <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

Reference to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.

### -param pnCsidl [out]

Type: <b>int*</b>

When this method returns, contains a pointer to the <a href="/windows/desktop/shell/csidl">CSIDL</a> value. This pointer is passed uninitialized.

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

To call this method, the caller must have at least User privileges.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-folderidfromcsidl">IKnownFolderManager::FolderIdFromCsidl</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>