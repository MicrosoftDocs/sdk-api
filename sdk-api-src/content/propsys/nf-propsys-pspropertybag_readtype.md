---
UID: NF:propsys.PSPropertyBag_ReadType
title: PSPropertyBag_ReadType function (propsys.h)
description: Reads the type of data value of a property that is stored in a property bag.
helpviewer_keywords: ["PSPropertyBag_ReadType","PSPropertyBag_ReadType function [Windows Properties]","properties.PSPropertyBag_ReadType","propsys/PSPropertyBag_ReadType","shell.PSPropertyBag_ReadType","shell_PSPropertyBag_ReadType"]
old-location: properties\PSPropertyBag_ReadType.htm
tech.root: properties
ms.assetid: 826038F7-FD93-474e-BCA7-910E214F3E01
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadType, PSPropertyBag_ReadType function [Windows Properties], properties.PSPropertyBag_ReadType, propsys/PSPropertyBag_ReadType, shell.PSPropertyBag_ReadType, shell_PSPropertyBag_ReadType
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
 - PSPropertyBag_ReadType
 - propsys/PSPropertyBag_ReadType
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
 - PSPropertyBag_ReadType
---

# PSPropertyBag_ReadType function


## -description

Reads the type of data value of a property that is stored in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object, that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.

### -param var [out]

Type: <b>VARIANT*</b>

Returns on successful function completion a pointer to a <b>VARIANT</b> data type that contains the property value.

### -param type [out]

Type: <b>VARTYPE*</b>

If <i>type</i> is VT_EMPTY, this function reads the <b>VARIANT</b> of the property in the IPropertyBag   <i>propBag</i> parameter. If <i>type</i> is not VT_EMPTY and not the same as the <b>VARIANT</b> read, then this function attempts to convert the <b>VARIANT</b> read to the <b>VARTYPE</b> defined by <i>type</i> parameter before returning.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> and <a href="../ocidl/nn-ocidl-ipersistpropertybag.md">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768194(v=vs.85)">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768195(v=vs.85)">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_delete">PSPropertyBag_Delete</a>