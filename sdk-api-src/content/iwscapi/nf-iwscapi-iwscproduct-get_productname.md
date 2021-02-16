---
UID: NF:iwscapi.IWscProduct.get_ProductName
title: IWscProduct::get_ProductName (iwscapi.h)
description: Returns the current product information for the security product.
helpviewer_keywords: ["IWscProduct interface [Windows API]","get_ProductName method","IWscProduct.get_ProductName","IWscProduct::get_ProductName","get_ProductName","get_ProductName method [Windows API]","get_ProductName method [Windows API]","IWscProduct interface","iwscapi/IWscProduct::get_ProductName","winprog.iwscproduct_productname"]
old-location: winprog\iwscproduct_productname.htm
tech.root: winprog
ms.assetid: 5270D8AF-AA69-4CC8-8ABC-F0716B3ED588
ms.date: 12/05/2018
ms.keywords: IWscProduct interface [Windows API],get_ProductName method, IWscProduct.get_ProductName, IWscProduct::get_ProductName, get_ProductName, get_ProductName method [Windows API], get_ProductName method [Windows API],IWscProduct interface, iwscapi/IWscProduct::get_ProductName, winprog.iwscproduct_productname
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
 - IWscProduct::get_ProductName
 - iwscapi/IWscProduct::get_ProductName
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
 - IWscProduct.get_ProductName
---

# IWscProduct::get_ProductName


## -description

Returns the current product information for the security product.

## -parameters

### -param pVal [out]

A pointer to the name of the security product. This is displayed in the Windows Security Center user interface.

## -returns

If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.

## -see-also

<a href="/windows/desktop/api/iwscapi/nn-iwscapi-iwscproduct">IWscProduct</a>