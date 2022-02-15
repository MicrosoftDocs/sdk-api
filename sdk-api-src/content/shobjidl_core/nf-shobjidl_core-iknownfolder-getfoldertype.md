---
UID: NF:shobjidl_core.IKnownFolder.GetFolderType
title: IKnownFolder::GetFolderType (shobjidl_core.h)
description: Retrieves the folder type.
helpviewer_keywords: ["GetFolderType","GetFolderType method [Windows Shell]","GetFolderType method [Windows Shell]","IKnownFolder interface","IKnownFolder interface [Windows Shell]","GetFolderType method","IKnownFolder.GetFolderType","IKnownFolder::GetFolderType","_shell_IKnownFolder_GetFolderType","shell.IKnownFolder_GetFolderType","shobjidl_core/IKnownFolder::GetFolderType"]
old-location: shell\IKnownFolder_GetFolderType.htm
tech.root: shell
ms.assetid: a2457d52-390d-43bd-8db0-9c18492cc40e
ms.date: 12/05/2018
ms.keywords: GetFolderType, GetFolderType method [Windows Shell], GetFolderType method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetFolderType method, IKnownFolder.GetFolderType, IKnownFolder::GetFolderType, _shell_IKnownFolder_GetFolderType, shell.IKnownFolder_GetFolderType, shobjidl_core/IKnownFolder::GetFolderType
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
 - IKnownFolder::GetFolderType
 - shobjidl_core/IKnownFolder::GetFolderType
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
 - IKnownFolder.GetFolderType
---

# IKnownFolder::GetFolderType


## -description

Retrieves the folder type.

## -parameters

### -param pftid [out]

Type: <b><a href="/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a>*</b>

When this returns, contains a pointer to a <a href="/windows/desktop/shell/foldertypeid">FOLDERTYPEID</a> (a GUID) that identifies the known folder type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>