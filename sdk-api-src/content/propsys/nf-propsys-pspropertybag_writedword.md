---
UID: NF:propsys.PSPropertyBag_WriteDWORD
title: PSPropertyBag_WriteDWORD function (propsys.h)
description: Sets the DWORD value of a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_WriteDWORD","PSPropertyBag_WriteDWORD function [Windows Properties]","properties.PSPropertyBag_WriteDWORD","propsys/PSPropertyBag_WriteDWORD","shell.PSPropertyBag_WriteDWORD","shell_PSPropertyBag_WriteDWORD"]
old-location: properties\PSPropertyBag_WriteDWORD.htm
tech.root: properties
ms.assetid: 59142C21-032F-462c-B4A7-337483917ABC
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteDWORD, PSPropertyBag_WriteDWORD function [Windows Properties], properties.PSPropertyBag_WriteDWORD, propsys/PSPropertyBag_WriteDWORD, shell.PSPropertyBag_WriteDWORD, shell_PSPropertyBag_WriteDWORD
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
 - PSPropertyBag_WriteDWORD
 - propsys/PSPropertyBag_WriteDWORD
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
 - PSPropertyBag_WriteDWORD
---

# PSPropertyBag_WriteDWORD function


## -description

Sets the <b>DWORD</b> value of a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [in]

Type: <b>DWORD</b>

A <b>DWORD</b> value to which the named property should be set.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readdword">PSPropertyBag_ReadDWORD</a>