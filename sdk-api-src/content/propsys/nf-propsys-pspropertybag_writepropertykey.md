---
UID: NF:propsys.PSPropertyBag_WritePropertyKey
title: PSPropertyBag_WritePropertyKey function (propsys.h)
description: Sets the property key value of a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_WritePropertyKey","PSPropertyBag_WritePropertyKey function [Windows Properties]","properties.PSPropertyBag_WritePropertyKey","propsys/PSPropertyBag_WritePropertyKey","shell.PSPropertyBag_WritePropertyKey"]
old-location: properties\PSPropertyBag_WritePropertyKey.htm
tech.root: properties
ms.assetid: 52965079-ECC6-411a-BBB9-4EA2B7C01631
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WritePropertyKey, PSPropertyBag_WritePropertyKey function [Windows Properties], properties.PSPropertyBag_WritePropertyKey, propsys/PSPropertyBag_WritePropertyKey, shell.PSPropertyBag_WritePropertyKey
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
 - PSPropertyBag_WritePropertyKey
 - propsys/PSPropertyBag_WritePropertyKey
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
 - PSPropertyBag_WritePropertyKey
---

# PSPropertyBag_WritePropertyKey function


## -description

Sets the property key value of a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [in]

Type: <b>REFPROPERTYKEY</b>

A <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that specifies the property key value to store in the property.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Property keys uniquely identify a property. For example, <code>PKEY_Keywords</code> corresponds to <code>System.Keywords</code>. This function succeeds only for properties registered as part of the property schema.

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readpropertykey">PSPropertyBag_ReadPropertyKey</a>