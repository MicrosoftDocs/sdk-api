---
UID: NF:propsys.PSPropertyBag_ReadBOOL
title: PSPropertyBag_ReadBOOL function (propsys.h)
description: Reads the BOOL data value of a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_ReadBOOL","PSPropertyBag_ReadBOOL function [Windows Properties]","properties.PSPropertyBag_ReadBOOL","propsys/PSPropertyBag_ReadBOOL","shell.PSPropertyBag_ReadBOOL","shell_PSPropertyBag_ReadBOOL"]
old-location: properties\PSPropertyBag_ReadBOOL.htm
tech.root: properties
ms.assetid: 95F9CB5E-E690-4d83-A094-02981F0578CF
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadBOOL, PSPropertyBag_ReadBOOL function [Windows Properties], properties.PSPropertyBag_ReadBOOL, propsys/PSPropertyBag_ReadBOOL, shell.PSPropertyBag_ReadBOOL, shell_PSPropertyBag_ReadBOOL
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
 - PSPropertyBag_ReadBOOL
 - propsys/PSPropertyBag_ReadBOOL
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
 - PSPropertyBag_ReadBOOL
---

# PSPropertyBag_ReadBOOL function


## -description

Reads the <b>BOOL</b> data value of a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [out]

Type: <b>BOOL*</b>

When this function returns successfully, contains a pointer to the value read from the property.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

The property bag property function API converts between windows types and the <b>VARIANT</b> type that is used to express values in a property bag.  Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertysystem">PSGetPropertySystem</a>



<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_writebool">PSPropertyBag_WriteBOOL</a>