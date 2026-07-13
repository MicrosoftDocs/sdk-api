---
UID: NF:propsys.PSPropertyBag_WriteLONG
title: PSPropertyBag_WriteLONG function (propsys.h)
description: Sets the LONG value of a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_WriteLONG","PSPropertyBag_WriteLONG function [Windows Properties]","properties.PSPropertyBag_WriteLONG","propsys/PSPropertyBag_WriteLONG","shell.PSPropertyBag_WriteLONG","shell_PSPropertyBag_WriteLONG"]
old-location: properties\PSPropertyBag_WriteLONG.htm
tech.root: properties
ms.assetid: A623D097-FEF8-4864-A80A-C6EF824EC245
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteLONG, PSPropertyBag_WriteLONG function [Windows Properties], properties.PSPropertyBag_WriteLONG, propsys/PSPropertyBag_WriteLONG, shell.PSPropertyBag_WriteLONG, shell_PSPropertyBag_WriteLONG
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSPropertyBag_WriteLONG
 - propsys/PSPropertyBag_WriteLONG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSPropertyBag_WriteLONG
---

# PSPropertyBag_WriteLONG function


## -description

Sets the <b>LONG</b> value of a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [in]

Type: <b>LONG</b>

The <b>LONG</b> value to which the property should be set.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readlong">PSPropertyBag_ReadLONG</a>