---
UID: NF:propvarutil.VariantToUInt32Array
title: VariantToUInt32Array function (propvarutil.h)
description: Extracts data from a vector structure into an unsigned Int32 array.
helpviewer_keywords: ["VariantToUInt32Array","VariantToUInt32Array function [Windows Properties]","_shell_VariantToUInt32Array","properties.VariantToUInt32Array","propvarutil/VariantToUInt32Array","shell.VariantToUInt32Array"]
old-location: properties\VariantToUInt32Array.htm
tech.root: properties
ms.assetid: 506a02f8-6390-44a0-9f14-bfc8fb7ad180
ms.date: 12/05/2018
ms.keywords: VariantToUInt32Array, VariantToUInt32Array function [Windows Properties], _shell_VariantToUInt32Array, properties.VariantToUInt32Array, propvarutil/VariantToUInt32Array, shell.VariantToUInt32Array
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
 - VariantToUInt32Array
 - propvarutil/VariantToUInt32Array
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
 - VariantToUInt32Array
---

# VariantToUInt32Array function


## -description

Extracts data from a vector structure into an unsigned <b>Int32</b> array.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param prgn [out]

Type: <b>ULONG*</b>

Pointer to the unsigned <b>Int32</b> data extracted from source variant structure.

### -param crgn [in]

Type: <b>ULONG</b>

Specifies unsigned <b>Int32</b> array size.

### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of unsigned <b>Int32</b> elements extracted from source variant structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

