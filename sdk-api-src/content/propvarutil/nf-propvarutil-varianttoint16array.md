---
UID: NF:propvarutil.VariantToInt16Array
title: VariantToInt16Array function (propvarutil.h)
description: Extracts data from a vector structure into an Int16 array.
helpviewer_keywords: ["VariantToInt16Array","VariantToInt16Array function [Windows Properties]","_shell_VariantToInt16Array","properties.VariantToInt16Array","propvarutil/VariantToInt16Array","shell.VariantToInt16Array"]
old-location: properties\VariantToInt16Array.htm
tech.root: properties
ms.assetid: dd00d986-acfa-445e-a0f6-0f52860b762b
ms.date: 12/05/2018
ms.keywords: VariantToInt16Array, VariantToInt16Array function [Windows Properties], _shell_VariantToInt16Array, properties.VariantToInt16Array, propvarutil/VariantToInt16Array, shell.VariantToInt16Array
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
 - VariantToInt16Array
 - propvarutil/VariantToInt16Array
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
 - VariantToInt16Array
---

# VariantToInt16Array function


## -description

Extracts data from a vector structure into an <b>Int16</b> array.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param prgn [out]

Type: <b>SHORT*</b>

Pointer to the <b>Int16</b> data extracted from source variant structure.

### -param crgn [in]

Type: <b>ULONG</b>

Specifies <b>Int16</b> array size.

### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of <b>Int16</b> elements extracted from source variant structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

