---
UID: NF:shobjidl_core.IShellItemResources.OpenResource
title: IShellItemResources::OpenResource (shobjidl_core.h)
description: Opens a specified resource.
helpviewer_keywords: ["IShellItemResources interface [Windows Shell]","OpenResource method","IShellItemResources.OpenResource","IShellItemResources::OpenResource","OpenResource","OpenResource method [Windows Shell]","OpenResource method [Windows Shell]","IShellItemResources interface","_shell_IShellItemResources_OpenResource","shell.IShellItemResources_OpenResource","shobjidl_core/IShellItemResources::OpenResource"]
old-location: shell\IShellItemResources_OpenResource.htm
tech.root: shell
ms.assetid: abef9009-7e0d-4a09-aba8-2b391e4ab487
ms.date: 12/05/2018
ms.keywords: IShellItemResources interface [Windows Shell],OpenResource method, IShellItemResources.OpenResource, IShellItemResources::OpenResource, OpenResource, OpenResource method [Windows Shell], OpenResource method [Windows Shell],IShellItemResources interface, _shell_IShellItemResources_OpenResource, shell.IShellItemResources_OpenResource, shobjidl_core/IShellItemResources::OpenResource
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
 - IShellItemResources::OpenResource
 - shobjidl_core/IShellItemResources::OpenResource
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
 - IShellItemResources.OpenResource
---

# IShellItemResources::OpenResource


## -description

Opens a specified resource.

## -parameters

### -param pcsir [in]

Type: <b>const <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a> resource.

### -param riid [in]

Type: <b>REFIID</b>

A reference to a desired IID.

### -param ppv [out]

Type: <b>void**</b>

The address of a pointer to a resource.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.