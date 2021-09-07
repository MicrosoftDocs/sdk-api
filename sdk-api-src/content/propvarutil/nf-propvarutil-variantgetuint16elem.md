---
UID: NF:propvarutil.VariantGetUInt16Elem
title: VariantGetUInt16Elem function (propvarutil.h)
description: Extracts a single unsigned Int16 element from a variant structure.
helpviewer_keywords: ["VariantGetUInt16Elem","VariantGetUInt16Elem function [Windows Properties]","_shell_VariantGetUInt16Elem","properties.VariantGetUInt16Elem","propvarutil/VariantGetUInt16Elem","shell.VariantGetUInt16Elem"]
old-location: properties\VariantGetUInt16Elem.htm
tech.root: properties
ms.assetid: 6d2a8b0b-bcd2-4bad-a006-2443eabd7a16
ms.date: 12/05/2018
ms.keywords: VariantGetUInt16Elem, VariantGetUInt16Elem function [Windows Properties], _shell_VariantGetUInt16Elem, properties.VariantGetUInt16Elem, propvarutil/VariantGetUInt16Elem, shell.VariantGetUInt16Elem
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - VariantGetUInt16Elem
 - propvarutil/VariantGetUInt16Elem
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
 - VariantGetUInt16Elem
---

# VariantGetUInt16Elem function


## -description

Extracts a single unsigned <b>Int16</b> element from a variant structure.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param iElem [in]

Type: <b>ULONG</b>

Specifies a vector or array index; otherwise, value must be 0.

### -param pnVal [out]

Type: <b>USHORT*</b>

Pointer to the extracted element value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

