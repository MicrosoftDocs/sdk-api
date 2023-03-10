---
UID: NF:shobjidl_core.IEnumResources.Clone
title: IEnumResources::Clone (shobjidl_core.h)
description: Clones a resource enumerator.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","IEnumResources interface","IEnumResources interface [Windows Shell]","Clone method","IEnumResources.Clone","IEnumResources::Clone","_shell_IEnumResources_Clone","shell.IEnumResources_Clone","shobjidl_core/IEnumResources::Clone"]
old-location: shell\IEnumResources_Clone.htm
tech.root: shell
ms.assetid: 660243ba-263d-4f4a-b26f-ab831f60d76b
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumResources interface, IEnumResources interface [Windows Shell],Clone method, IEnumResources.Clone, IEnumResources::Clone, _shell_IEnumResources_Clone, shell.IEnumResources_Clone, shobjidl_core/IEnumResources::Clone
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
 - IEnumResources::Clone
 - shobjidl_core/IEnumResources::Clone
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
 - IEnumResources.Clone
---

# IEnumResources::Clone


## -description

Clones a resource enumerator.

## -parameters

### -param ppenumr [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources">IEnumResources</a>**</b>

Contains the address of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources">IEnumResources</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.