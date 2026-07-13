---
UID: NF:shobjidl_core.IParseAndCreateItem.SetItem
title: IParseAndCreateItem::SetItem (shobjidl_core.h)
description: IParseAndCreateItem::SetItem method
helpviewer_keywords: ["IParseAndCreateItem interface [Windows Shell]","SetItem method","IParseAndCreateItem.SetItem","IParseAndCreateItem::SetItem","SetItem","SetItem method [Windows Shell]","SetItem method [Windows Shell]","IParseAndCreateItem interface","_shell_IParseAndCreateItem_SetItem","shell.IParseAndCreateItem_SetItem","shobjidl_core/IParseAndCreateItem::SetItem"]
old-location: shell\IParseAndCreateItem_SetItem.htm
tech.root: shell
ms.assetid: 4a9f2d58-2959-40bd-ba82-74ca0e504145
ms.date: 12/05/2018
ms.keywords: IParseAndCreateItem interface [Windows Shell],SetItem method, IParseAndCreateItem.SetItem, IParseAndCreateItem::SetItem, SetItem, SetItem method [Windows Shell], SetItem method [Windows Shell],IParseAndCreateItem interface, _shell_IParseAndCreateItem_SetItem, shell.IParseAndCreateItem_SetItem, shobjidl_core/IParseAndCreateItem::SetItem
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IParseAndCreateItem::SetItem
 - shobjidl_core/IParseAndCreateItem::SetItem
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
 - IParseAndCreateItem.SetItem
---

# IParseAndCreateItem::SetItem


## -description

Sets a Shell item that [SHCreateItemFromParsingName](./nf-shobjidl_core-shcreateitemfromparsingname.md) created from a parsing name.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem">IParseAndCreateItem</a>