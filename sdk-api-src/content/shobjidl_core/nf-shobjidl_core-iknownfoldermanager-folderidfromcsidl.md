---
UID: NF:shobjidl_core.IKnownFolderManager.FolderIdFromCsidl
title: IKnownFolderManager::FolderIdFromCsidl (shobjidl_core.h)
description: Gets the KNOWNFOLDERID that is the equivalent of a legacy CSIDL value.
helpviewer_keywords: ["FolderIdFromCsidl","FolderIdFromCsidl method [Windows Shell]","FolderIdFromCsidl method [Windows Shell]","IKnownFolderManager interface","IKnownFolderManager interface [Windows Shell]","FolderIdFromCsidl method","IKnownFolderManager.FolderIdFromCsidl","IKnownFolderManager::FolderIdFromCsidl","_shell_IKnownFolderManager_FolderIdFromCsidl","shell.IKnownFolderManager_FolderIdFromCsidl","shobjidl_core/IKnownFolderManager::FolderIdFromCsidl"]
old-location: shell\IKnownFolderManager_FolderIdFromCsidl.htm
tech.root: shell
ms.assetid: 8c819558-8cbd-4576-98e6-99efa39ca5a6
ms.date: 12/05/2018
ms.keywords: FolderIdFromCsidl, FolderIdFromCsidl method [Windows Shell], FolderIdFromCsidl method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FolderIdFromCsidl method, IKnownFolderManager.FolderIdFromCsidl, IKnownFolderManager::FolderIdFromCsidl, _shell_IKnownFolderManager_FolderIdFromCsidl, shell.IKnownFolderManager_FolderIdFromCsidl, shobjidl_core/IKnownFolderManager::FolderIdFromCsidl
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
 - IKnownFolderManager::FolderIdFromCsidl
 - shobjidl_core/IKnownFolderManager::FolderIdFromCsidl
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
 - IKnownFolderManager.FolderIdFromCsidl
---

# IKnownFolderManager::FolderIdFromCsidl


## -description

Gets the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that is the equivalent of a legacy <a href="/windows/desktop/shell/csidl">CSIDL</a> value.

## -parameters

### -param nCsidl [in]

Type: <b>int</b>

The <a href="/windows/desktop/shell/csidl">CSIDL</a> value.

### -param pfid [out]

Type: <b><a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>*</b>

When this method returns, contains a pointer to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>. This pointer is passed uninitialized.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To call this method, the caller must have at least User privileges.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-folderidtocsidl">IKnownFolderManager::FolderIdToCsidl</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>