---
UID: NF:propvarutil.VariantToInt64ArrayAlloc
title: VariantToInt64ArrayAlloc function (propvarutil.h)
description: Extracts data from a vector structure into a newly-allocated Int64 array.
helpviewer_keywords: ["VariantToInt64ArrayAlloc","VariantToInt64ArrayAlloc function [Windows Properties]","_shell_VariantToInt64ArrayAlloc","properties.VariantToInt64ArrayAlloc","propvarutil/VariantToInt64ArrayAlloc","shell.VariantToInt64ArrayAlloc"]
old-location: properties\VariantToInt64ArrayAlloc.htm
tech.root: properties
ms.assetid: 15a583bd-fdef-4802-a18b-0a21b9be5448
ms.date: 12/05/2018
ms.keywords: VariantToInt64ArrayAlloc, VariantToInt64ArrayAlloc function [Windows Properties], _shell_VariantToInt64ArrayAlloc, properties.VariantToInt64ArrayAlloc, propvarutil/VariantToInt64ArrayAlloc, shell.VariantToInt64ArrayAlloc
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
 - VariantToInt64ArrayAlloc
 - propvarutil/VariantToInt64ArrayAlloc
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
 - VariantToInt64ArrayAlloc
---

# VariantToInt64ArrayAlloc function


## -description

Extracts data from a vector structure into a newly-allocated <b>Int64</b> array.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pprgn [out]

Type: <b>LONGLONG**</b>

Pointer to the address of the <b>Int64</b> data extracted from source variant structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of <b>Int64</b> elements extracted from source variant structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

