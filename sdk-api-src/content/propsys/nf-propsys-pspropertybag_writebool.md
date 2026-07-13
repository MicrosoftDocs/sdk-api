---
UID: NF:propsys.PSPropertyBag_WriteBOOL
title: PSPropertyBag_WriteBOOL function (propsys.h)
description: Sets the BOOL value of a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_WriteBOOL","PSPropertyBag_WriteBOOL function [Windows Properties]","properties.PSPropertyBag_WriteBOOL","propsys/PSPropertyBag_WriteBOOL","shell.PSPropertyBag_WriteBOOL","shell_PSPropertyBag_WriteBOOL"]
old-location: properties\PSPropertyBag_WriteBOOL.htm
tech.root: properties
ms.assetid: 3703A7C4-CFDC-4453-AA8F-6A5D6B7D3E66
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteBOOL, PSPropertyBag_WriteBOOL function [Windows Properties], properties.PSPropertyBag_WriteBOOL, propsys/PSPropertyBag_WriteBOOL, shell.PSPropertyBag_WriteBOOL, shell_PSPropertyBag_WriteBOOL
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
 - PSPropertyBag_WriteBOOL
 - propsys/PSPropertyBag_WriteBOOL
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
 - PSPropertyBag_WriteBOOL
---

# PSPropertyBag_WriteBOOL function


## -description

Sets the <b>BOOL</b> value of a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [in]

Type: <b>BOOL</b>

The <b>BOOL</b> value to which the named property should be set.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readbool">PSPropertyBag_ReadBOOL</a>