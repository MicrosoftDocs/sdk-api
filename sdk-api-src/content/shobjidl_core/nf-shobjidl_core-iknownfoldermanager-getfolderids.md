---
UID: NF:shobjidl_core.IKnownFolderManager.GetFolderIds
title: IKnownFolderManager::GetFolderIds (shobjidl_core.h)
description: Gets an array of all registered known folder IDs. This can be used in enumerating all known folders.
helpviewer_keywords: ["GetFolderIds","GetFolderIds method [Windows Shell]","GetFolderIds method [Windows Shell]","IKnownFolderManager interface","IKnownFolderManager interface [Windows Shell]","GetFolderIds method","IKnownFolderManager.GetFolderIds","IKnownFolderManager::GetFolderIds","_shell_IKnownFolderManager_GetFolderIds","shell.IKnownFolderManager_GetFolderIds","shobjidl_core/IKnownFolderManager::GetFolderIds"]
old-location: shell\IKnownFolderManager_GetFolderIds.htm
tech.root: shell
ms.assetid: 3ac09fc4-15c4-4346-94ad-2a4617c463d1
ms.date: 12/05/2018
ms.keywords: GetFolderIds, GetFolderIds method [Windows Shell], GetFolderIds method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],GetFolderIds method, IKnownFolderManager.GetFolderIds, IKnownFolderManager::GetFolderIds, _shell_IKnownFolderManager_GetFolderIds, shell.IKnownFolderManager_GetFolderIds, shobjidl_core/IKnownFolderManager::GetFolderIds
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
 - IKnownFolderManager::GetFolderIds
 - shobjidl_core/IKnownFolderManager::GetFolderIds
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
 - IKnownFolderManager.GetFolderIds
---

# IKnownFolderManager::GetFolderIds


## -description

Gets an array of all registered known folder IDs. This can be used in enumerating all known folders.

## -parameters

### -param ppKFId [out]

Type: <b><a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>**</b>

When this method returns, contains a pointer to an array of all <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> values registered with the system. Use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to free these resources when they are no longer needed.

### -param pCount [in, out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> values in the array at <i>ppKFId</i>. The [in] functionality of this parameter is not used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller of this method must have User privileges.

You can use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-stringfromclsid">StringFromCLSID</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-stringfromguid2">StringFromGUID2</a> to convert the retrieved <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> values to strings.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>