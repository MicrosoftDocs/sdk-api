---
UID: NF:propsys.PSPropertyBag_ReadStrAlloc
title: PSPropertyBag_ReadStrAlloc function (propsys.h)
description: Reads a string data value from a property in a property bag and allocates memory for the string that is read.
helpviewer_keywords: ["PSPropertyBag_ReadStrAlloc","PSPropertyBag_ReadStrAlloc function [Windows Properties]","properties.PSPropertyBag_ReadStrAlloc","propsys/PSPropertyBag_ReadStrAlloc","shell.PSPropertyBag_ReadStrAlloc","shell_PSPropertyBag_ReadStrAlloc"]
old-location: properties\PSPropertyBag_ReadStrAlloc.htm
tech.root: properties
ms.assetid: 2F58A6DB-3563-42fa-9B6F-327D0A87AE81
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadStrAlloc, PSPropertyBag_ReadStrAlloc function [Windows Properties], properties.PSPropertyBag_ReadStrAlloc, propsys/PSPropertyBag_ReadStrAlloc, shell.PSPropertyBag_ReadStrAlloc, shell_PSPropertyBag_ReadStrAlloc
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
 - PSPropertyBag_ReadStrAlloc
 - propsys/PSPropertyBag_ReadStrAlloc
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
 - PSPropertyBag_ReadStrAlloc
---

# PSPropertyBag_ReadStrAlloc function


## -description

Reads a string data value from a property in a property bag and allocates memory for the string that is read.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.

### -param value [out]

Type: <b>PWSTR*</b>

When this function returns, contains a pointer to a string data value from a property in a property bag and allocates memory for the string that is read. The caller of the <a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readstralloc">PSPropertyBag_ReadStrAlloc</a> function needs to call a <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function on this parameter.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.