---
UID: NF:shobjidl_core.IParseAndCreateItem.GetItem
title: IParseAndCreateItem::GetItem (shobjidl_core.h)
description: IParseAndCreateItem::GetItem method
helpviewer_keywords: ["GetItem","GetItem method [Windows Shell]","GetItem method [Windows Shell]","IParseAndCreateItem interface","IParseAndCreateItem interface [Windows Shell]","GetItem method","IParseAndCreateItem.GetItem","IParseAndCreateItem::GetItem","_shell_IParseAndCreateItem_GetItem","shell.IParseAndCreateItem_GetItem","shobjidl_core/IParseAndCreateItem::GetItem"]
old-location: shell\IParseAndCreateItem_GetItem.htm
tech.root: shell
ms.assetid: 7071621c-8311-45a2-afd5-144bcf707727
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Shell], GetItem method [Windows Shell],IParseAndCreateItem interface, IParseAndCreateItem interface [Windows Shell],GetItem method, IParseAndCreateItem.GetItem, IParseAndCreateItem::GetItem, _shell_IParseAndCreateItem_GetItem, shell.IParseAndCreateItem_GetItem, shobjidl_core/IParseAndCreateItem::GetItem
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
 - IParseAndCreateItem::GetItem
 - shobjidl_core/IParseAndCreateItem::GetItem
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
 - IParseAndCreateItem.GetItem
---

# IParseAndCreateItem::GetItem


## -description

Gets a stored Shell item that [SHCreateItemFromParsingName](./nf-shobjidl_core-shcreateitemfromparsingname.md) created from a parsing name.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_IShellItem.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem">IParseAndCreateItem</a>