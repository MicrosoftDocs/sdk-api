---
UID: NF:propvarutil.VariantToStringArrayAlloc
title: VariantToStringArrayAlloc function (propvarutil.h)
description: Extracts data from a vector structure into a newly-allocated String array.
helpviewer_keywords: ["VariantToStringArrayAlloc","VariantToStringArrayAlloc function [Windows Properties]","_shell_VariantToStringArrayAlloc","properties.VariantToStringArrayAlloc","propvarutil/VariantToStringArrayAlloc","shell.VariantToStringArrayAlloc"]
old-location: properties\VariantToStringArrayAlloc.htm
tech.root: properties
ms.assetid: 2725b824-b26c-4b33-bc18-a6f4c0ef74e6
ms.date: 12/05/2018
ms.keywords: VariantToStringArrayAlloc, VariantToStringArrayAlloc function [Windows Properties], _shell_VariantToStringArrayAlloc, properties.VariantToStringArrayAlloc, propvarutil/VariantToStringArrayAlloc, shell.VariantToStringArrayAlloc
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
 - VariantToStringArrayAlloc
 - propvarutil/VariantToStringArrayAlloc
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
 - VariantToStringArrayAlloc
---

# VariantToStringArrayAlloc function


## -description

Extracts data from a vector structure into a newly-allocated String array.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pprgsz [out]

Type: <b>PWSTR**</b>

The address of a pointer to the string data extracted from source variant structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of string elements extracted from source variant structure.


#### - crgsz [in]

Type: <b>ULONG</b>

Specifies string array size.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

