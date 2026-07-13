---
UID: NF:propvarutil.VariantToUInt16Array
title: VariantToUInt16Array function (propvarutil.h)
description: Extracts data from a vector structure into an unsigned Int16 array.
helpviewer_keywords: ["VariantToUInt16Array","VariantToUInt16Array function [Windows Properties]","_shell_VariantToUInt16Array","properties.VariantToUInt16Array","propvarutil/VariantToUInt16Array","shell.VariantToUInt16Array"]
old-location: properties\VariantToUInt16Array.htm
tech.root: properties
ms.assetid: 8da12aa7-f54e-4a38-b9bb-0dd019f8823b
ms.date: 12/05/2018
ms.keywords: VariantToUInt16Array, VariantToUInt16Array function [Windows Properties], _shell_VariantToUInt16Array, properties.VariantToUInt16Array, propvarutil/VariantToUInt16Array, shell.VariantToUInt16Array
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
 - VariantToUInt16Array
 - propvarutil/VariantToUInt16Array
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
 - VariantToUInt16Array
---

# VariantToUInt16Array function


## -description

Extracts data from a vector structure into an unsigned <b>Int16</b> array.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param prgn [out]

Type: <b>USHORT*</b>

Pointer to the unsigned <b>Int16</b> data extracted from source variant structure.

### -param crgn [in]

Type: <b>ULONG</b>

Specifies unsigned <b>Int16</b> array size.

### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of unsigned <b>Int16</b> elements extracted from source variant structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

