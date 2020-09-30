---
UID: NF:propsys.PSPropertyBag_ReadGUID
title: PSPropertyBag_ReadGUID function (propsys.h)
description: Reads the GUID data value from a property in a property bag.
helpviewer_keywords: ["PSPropertyBag_ReadGUID","PSPropertyBag_ReadGUID function [Windows Properties]","properties.PSPropertyBag_ReadGUID","propsys/PSPropertyBag_ReadGUID","shell.PSPropertyBag_ReadGUID","shell_PSPropertyBag_ReadGUID"]
old-location: properties\PSPropertyBag_ReadGUID.htm
tech.root: properties
ms.assetid: BCC6E830-CF05-42c1-874F-CCC97E58A4BC
ms.date: 12/05/2018
ms.keywords: PSPropertyBag_ReadGUID, PSPropertyBag_ReadGUID function [Windows Properties], properties.PSPropertyBag_ReadGUID, propsys/PSPropertyBag_ReadGUID, shell.PSPropertyBag_ReadGUID, shell_PSPropertyBag_ReadGUID
req.header: propsys.h
req.include-header: Propsys.idl
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
 - PSPropertyBag_ReadGUID
 - propsys/PSPropertyBag_ReadGUID
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
 - PSPropertyBag_ReadGUID
---

# PSPropertyBag_ReadGUID function


## -description

Reads the GUID data value from a property in a property bag.

## -parameters

### -param propBag [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a>*</b>

A pointer to an <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)">IPropertyBag</a> object that represents the property bag in which the property is stored.

### -param propName [in]

Type: <b>LPCWSTR</b>

A null-terminated property name string.

### -param value [out]

Type: <b>GUID*</b>

When this function returns, contains a pointer to a GUID property value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-pspropertybag_writeguid">PSPropertyBag_WriteGUID</a>