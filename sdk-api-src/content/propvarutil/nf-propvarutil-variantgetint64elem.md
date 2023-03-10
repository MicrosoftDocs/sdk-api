---
UID: NF:propvarutil.VariantGetInt64Elem
title: VariantGetInt64Elem function (propvarutil.h)
description: Extracts a single Int64 element from a variant structure.
helpviewer_keywords: ["VariantGetInt64Elem","VariantGetInt64Elem function [Windows Properties]","_shell_VariantGetInt64Elem","properties.VariantGetInt64Elem","propvarutil/VariantGetInt64Elem","shell.VariantGetInt64Elem"]
old-location: properties\VariantGetInt64Elem.htm
tech.root: properties
ms.assetid: 285705d3-3b8e-40ad-abf2-1adc5adda3d8
ms.date: 12/05/2018
ms.keywords: VariantGetInt64Elem, VariantGetInt64Elem function [Windows Properties], _shell_VariantGetInt64Elem, properties.VariantGetInt64Elem, propvarutil/VariantGetInt64Elem, shell.VariantGetInt64Elem
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
 - VariantGetInt64Elem
 - propvarutil/VariantGetInt64Elem
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
 - VariantGetInt64Elem
---

# VariantGetInt64Elem function


## -description

Extracts a single <b>Int64</b> element from a variant structure.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, value must be 0.

### -param pnVal [out]

Type: <b>LONGLONG*</b>

Pointer to the extracted element value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

