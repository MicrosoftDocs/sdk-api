---
UID: NF:propsys.PSPropertyBag_ReadInt
title: PSPropertyBag_ReadInt function (propsys.h)
description: Reads an int data value from a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_ReadInt","PSPropertyBag_ReadInt function [Windows Properties]","properties.PSPropertyBag_ReadInt","propsys/PSPropertyBag_ReadInt","shell.PSPropertyBag_ReadInt","shell_PSPropertyBag_ReadInt"]
old-location: properties\PSPropertyBag_ReadInt.htm
tech.root: properties
ms.assetid: 9CEC97E6-C88F-4182-876C-D77EA14915DA
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadInt, PSPropertyBag_ReadInt function [Windows Properties], properties.PSPropertyBag_ReadInt, propsys/PSPropertyBag_ReadInt, shell.PSPropertyBag_ReadInt, shell_PSPropertyBag_ReadInt
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
 - PSPropertyBag_ReadInt
 - propsys/PSPropertyBag_ReadInt
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
 - PSPropertyBag_ReadInt
---

# PSPropertyBag_ReadInt function


## -description

Reads an <b>int</b> data value from a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [out]

Type: <b>int*</b>

When this function returns, contains a pointer to an <b>int</b> property value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the property bag does not already contain the specified property, the call still succeeds.

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_writeint">PSPropertyBag_WriteInt</a>