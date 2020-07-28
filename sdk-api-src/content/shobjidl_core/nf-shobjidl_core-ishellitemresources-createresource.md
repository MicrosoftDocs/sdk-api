---
UID: NF:shobjidl_core.IShellItemResources.CreateResource
title: IShellItemResources::CreateResource (shobjidl_core.h)
description: Creates a specified resource.
helpviewer_keywords: ["CreateResource","CreateResource method [Windows Shell]","CreateResource method [Windows Shell]","IShellItemResources interface","IShellItemResources interface [Windows Shell]","CreateResource method","IShellItemResources.CreateResource","IShellItemResources::CreateResource","_shell_IShellItemResources_CreateResource","shell.IShellItemResources_CreateResource","shobjidl_core/IShellItemResources::CreateResource"]
old-location: shell\IShellItemResources_CreateResource.htm
tech.root: shell
ms.assetid: b854ee5f-ee4c-49e8-b0de-249154ec9b43
ms.date: 12/05/2018
ms.keywords: CreateResource, CreateResource method [Windows Shell], CreateResource method [Windows Shell],IShellItemResources interface, IShellItemResources interface [Windows Shell],CreateResource method, IShellItemResources.CreateResource, IShellItemResources::CreateResource, _shell_IShellItemResources_CreateResource, shell.IShellItemResources_CreateResource, shobjidl_core/IShellItemResources::CreateResource
f1_keywords:
- shobjidl_core/IShellItemResources.CreateResource
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IShellItemResources.CreateResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellItemResources::CreateResource


## -description


Creates a specified resource.


## -parameters




### -param pcsir [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shell_item_resource">SHELL_ITEM_RESOURCE</a> resource.


### -param riid [in]

Type: <b>REFIID</b>

A reference to a desired IID.


### -param ppv [out]

Type: <b>void**</b>

The address of a pointer to the resource.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



