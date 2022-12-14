---
UID: NF:propsys.PSPropertyBag_WriteUnknown
title: PSPropertyBag_WriteUnknown function (propsys.h)
description: Writes a property of an unknown data value in a property bag.
helpviewer_keywords: ["PSPropertyBag_WriteUnknown","PSPropertyBag_WriteUnknown function [Windows Properties]","properties.PSPropertyBag_WriteUnknown","propsys/PSPropertyBag_WriteUnknown","shell.PSPropertyBag_WriteUnknown","shell_PSPropertyBag_WriteUnknown"]
old-location: properties\PSPropertyBag_WriteUnknown.htm
tech.root: properties
ms.assetid: D96643E7-9A14-4410-BD2C-A264B74E0590
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_WriteUnknown, PSPropertyBag_WriteUnknown function [Windows Properties], properties.PSPropertyBag_WriteUnknown, propsys/PSPropertyBag_WriteUnknown, shell.PSPropertyBag_WriteUnknown, shell_PSPropertyBag_WriteUnknown
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
 - PSPropertyBag_WriteUnknown
 - propsys/PSPropertyBag_WriteUnknown
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
 - PSPropertyBag_WriteUnknown
---

# PSPropertyBag_WriteUnknown function


## -description

Writes a property of an unknown data value in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> derived interface that copies the specified property of an unknown data value in a property bag.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_readunknown">PSPropertyBag_ReadUnknown</a>