---
UID: NF:iwscapi.IWSCProductList.get_Item
title: IWSCProductList::get_Item (iwscapi.h)
description: Returns one of the types of providers on the computer.
helpviewer_keywords: ["IWSCProductList interface [Windows API]","get_Item method","IWSCProductList.get_Item","IWSCProductList::get_Item","get_Item","get_Item method [Windows API]","get_Item method [Windows API]","IWSCProductList interface","iwscapi/IWSCProductList::get_Item","winprog.iwscproductlist_item"]
old-location: winprog\iwscproductlist_item.htm
tech.root: winprog
ms.assetid: 041F45EF-BE1E-4C37-9BD7-ED9F45587ADA
ms.date: 12/05/2018
ms.keywords: IWSCProductList interface [Windows API],get_Item method, IWSCProductList.get_Item, IWSCProductList::get_Item, get_Item, get_Item method [Windows API], get_Item method [Windows API],IWSCProductList interface, iwscapi/IWSCProductList::get_Item, winprog.iwscproductlist_item
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSCProductList::get_Item
 - iwscapi/IWSCProductList::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wscapi.dll
api_name:
 - IWSCProductList.get_Item
---

# IWSCProductList::get_Item


## -description

Returns one of the  types of providers on the computer.

## -parameters

### -param index [in]

The list of the providers.

### -param pVal [out]

A pointer to the <a href="/windows/desktop/api/iwscapi/nn-iwscapi-iwscproduct">IWscProduct</a> product information.

## -returns

If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.

## -remarks

A provider is obtained by calling the <b>Item</b> method, which returns an interface pointer to an initialized <a href="/windows/desktop/api/iwscapi/nn-iwscapi-iwscproduct">IWscProduct</a> object.  The user is then able to retrieve the name, product state, and signature status through the methods of the <b>IWscProduct</b> interface.

## -see-also

<a href="/windows/desktop/api/iwscapi/nn-iwscapi-iwscproductlist">IWSCProductList</a>