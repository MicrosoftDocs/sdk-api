---
UID: NF:propsys.PSPropertyBag_WriteStream
title: PSPropertyBag_WriteStream function (propsys.h)
description: Writes a data stream to a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_WriteStream","PSPropertyBag_WriteStream function [Windows Properties]","properties.PSPropertyBag_WriteStream","propsys/PSPropertyBag_WriteStream","shell.PSPropertyBag_WriteStream","shell_PSPropertyBag_WriteStream"]
old-location: properties\PSPropertyBag_WriteStream.htm
tech.root: properties
ms.assetid: 48C3E7F7-ED7E-4797-A66A-A8529BF2A79C
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteStream, PSPropertyBag_WriteStream function [Windows Properties], properties.PSPropertyBag_WriteStream, propsys/PSPropertyBag_WriteStream, shell.PSPropertyBag_WriteStream, shell_PSPropertyBag_WriteStream
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
 - PSPropertyBag_WriteStream
 - propsys/PSPropertyBag_WriteStream
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
 - PSPropertyBag_WriteStream
---

# PSPropertyBag_WriteStream function


## -description

Writes a data stream to a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object to write to the property.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readstream">PSPropertyBag_ReadStream</a>