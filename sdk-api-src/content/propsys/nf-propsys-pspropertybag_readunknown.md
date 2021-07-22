---
UID: NF:propsys.PSPropertyBag_ReadUnknown
title: PSPropertyBag_ReadUnknown function (propsys.h)
description: Reads a given property of an unknown data value in a property bag.
helpviewer_keywords: ["PSPropertyBag_ReadUnknown","PSPropertyBag_ReadUnknown function [Windows Properties]","properties.PSPropertyBag_ReadUnknown","propsys/PSPropertyBag_ReadUnknown","shell.PSPropertyBag_ReadUnknown","shell_PSPropertyBag_ReadUnknown"]
old-location: properties\PSPropertyBag_ReadUnknown.htm
tech.root: properties
ms.assetid: 87921F52-308F-4ed7-8390-A3C0217ACEFD
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadUnknown, PSPropertyBag_ReadUnknown function [Windows Properties], properties.PSPropertyBag_ReadUnknown, propsys/PSPropertyBag_ReadUnknown, shell.PSPropertyBag_ReadUnknown, shell_PSPropertyBag_ReadUnknown
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
 - PSPropertyBag_ReadUnknown
 - propsys/PSPropertyBag_ReadUnknown
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
 - PSPropertyBag_ReadUnknown
---

# PSPropertyBag_ReadUnknown function


## -description

Reads a given property of an unknown data value in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object, that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>. This interface IID should be <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> or an interface derived from <b>IPropertyBag</b>.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> and <a href="../ocidl/nn-ocidl-ipersistpropertybag.md">IPersistPropertyBag</a> optimize Save As Text functionality. <b>IPropertyBag</b> and <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a> provide an object with a property bag in which the object can save its properties persistently. <b>IPropertyBag2</b> allows the object to obtain type information for each property: <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768194(v=vs.85)">IPropertyBag2::Read</a> causes one or more properties to be read from the property bag, and <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768195(v=vs.85)">IPropertyBag2::Write</a> causes one or more properties to be saved into the property bag.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_writeunknown">PSPropertyBag_WriteUnknown</a>