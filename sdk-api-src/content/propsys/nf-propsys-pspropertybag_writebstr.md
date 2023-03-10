---
UID: NF:propsys.PSPropertyBag_WriteBSTR
title: PSPropertyBag_WriteBSTR function (propsys.h)
description: Sets the BSTR value of a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_WriteBSTR","PSPropertyBag_WriteBSTR function [Windows Properties]","properties.PSPropertyBag_WriteBSTR","propsys/PSPropertyBag_WriteBSTR","shell.PSPropertyBag_WriteBSTR","shell_PSPropertyBag_WriteBSTR"]
old-location: properties\PSPropertyBag_WriteBSTR.htm
tech.root: properties
ms.assetid: 9C2DBD1F-6760-4812-A33E-9A71C5A421A9
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteBSTR, PSPropertyBag_WriteBSTR function [Windows Properties], properties.PSPropertyBag_WriteBSTR, propsys/PSPropertyBag_WriteBSTR, shell.PSPropertyBag_WriteBSTR, shell_PSPropertyBag_WriteBSTR
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
 - PSPropertyBag_WriteBSTR
 - propsys/PSPropertyBag_WriteBSTR
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
 - PSPropertyBag_WriteBSTR
---

# PSPropertyBag_WriteBSTR function


## -description

Sets the <b>BSTR</b> value of a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [in]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a></b>

The <b>BSTR</b> value to which the named property should be set.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readbstr">PSPropertyBag_ReadBSTR</a>