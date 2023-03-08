---
UID: NF:shobjidl_core.IKnownFolder.GetFolderDefinition
title: IKnownFolder::GetFolderDefinition (shobjidl_core.h)
description: Retrieves a structure that contains the defining elements of a known folder, which includes the folder's category, name, path, description, tooltip, icon, and other properties.
helpviewer_keywords: ["GetFolderDefinition","GetFolderDefinition method [Windows Shell]","GetFolderDefinition method [Windows Shell]","IKnownFolder interface","IKnownFolder interface [Windows Shell]","GetFolderDefinition method","IKnownFolder.GetFolderDefinition","IKnownFolder::GetFolderDefinition","_shell_IKnownFolder_GetFolderDefinition","shell.IKnownFolder_GetFolderDefinition","shobjidl_core/IKnownFolder::GetFolderDefinition"]
old-location: shell\IKnownFolder_GetFolderDefinition.htm
tech.root: shell
ms.assetid: b6f544cc-f487-405c-915d-b3a6dc59422c
ms.date: 12/05/2018
ms.keywords: GetFolderDefinition, GetFolderDefinition method [Windows Shell], GetFolderDefinition method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetFolderDefinition method, IKnownFolder.GetFolderDefinition, IKnownFolder::GetFolderDefinition, _shell_IKnownFolder_GetFolderDefinition, shell.IKnownFolder_GetFolderDefinition, shobjidl_core/IKnownFolder::GetFolderDefinition
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
 - IKnownFolder::GetFolderDefinition
 - shobjidl_core/IKnownFolder::GetFolderDefinition
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
 - IKnownFolder.GetFolderDefinition
---

# IKnownFolder::GetFolderDefinition


## -description

Retrieves a structure that contains the defining elements of a known folder, which includes the folder's category, name, path, description, tooltip, icon, and other properties.

## -parameters

### -param pKFD [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a>*</b>

When this method returns, contains a pointer to the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a> structure. When no longer needed, the calling application is responsible for calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields">FreeKnownFolderDefinitionFields</a> to free this resource.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a third-party application creates their own known folder, they do so by defining it with a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a> structure, then registering it with the system. Any registered known folder definition information—system-provided or application-created—can be retrieved through this method.

To call this method, the caller must have at least User privileges.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>