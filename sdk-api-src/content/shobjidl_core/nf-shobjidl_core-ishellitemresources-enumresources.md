---
UID: NF:shobjidl_core.IShellItemResources.EnumResources
title: IShellItemResources::EnumResources (shobjidl_core.h)
description: Gets a resource enumerator object.
helpviewer_keywords: ["EnumResources","EnumResources method [Windows Shell]","EnumResources method [Windows Shell]","IShellItemResources interface","IShellItemResources interface [Windows Shell]","EnumResources method","IShellItemResources.EnumResources","IShellItemResources::EnumResources","_shell_IShellItemResources_EnumResources","shell.IShellItemResources_EnumResources","shobjidl_core/IShellItemResources::EnumResources"]
old-location: shell\IShellItemResources_EnumResources.htm
tech.root: shell
ms.assetid: 29ac8ac9-4bd1-470c-885a-56f860d50a70
ms.date: 12/05/2018
ms.keywords: EnumResources, EnumResources method [Windows Shell], EnumResources method [Windows Shell],IShellItemResources interface, IShellItemResources interface [Windows Shell],EnumResources method, IShellItemResources.EnumResources, IShellItemResources::EnumResources, _shell_IShellItemResources_EnumResources, shell.IShellItemResources_EnumResources, shobjidl_core/IShellItemResources::EnumResources
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
 - IShellItemResources::EnumResources
 - shobjidl_core/IShellItemResources::EnumResources
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
 - IShellItemResources.EnumResources
---

# IShellItemResources::EnumResources


## -description

Gets a resource enumerator object.

## -parameters

### -param ppenumr [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources">IEnumResources</a>**</b>

The address of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources">IEnumResources</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.