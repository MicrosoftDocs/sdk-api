---
UID: NF:propvarutil.VariantToUInt16ArrayAlloc
title: VariantToUInt16ArrayAlloc function (propvarutil.h)
description: Extracts data from a vector structure into a newly-allocated unsigned Int16 array.
helpviewer_keywords: ["VariantToUInt16ArrayAlloc","VariantToUInt16ArrayAlloc function [Windows Properties]","_shell_VariantToUInt16ArrayAlloc","properties.VariantToUInt16ArrayAlloc","propvarutil/VariantToUInt16ArrayAlloc","shell.VariantToUInt16ArrayAlloc"]
old-location: properties\VariantToUInt16ArrayAlloc.htm
tech.root: properties
ms.assetid: 59e8d295-3be4-4e9a-a096-ead777d3aa8a
ms.date: 12/05/2018
ms.keywords: VariantToUInt16ArrayAlloc, VariantToUInt16ArrayAlloc function [Windows Properties], _shell_VariantToUInt16ArrayAlloc, properties.VariantToUInt16ArrayAlloc, propvarutil/VariantToUInt16ArrayAlloc, shell.VariantToUInt16ArrayAlloc
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
 - VariantToUInt16ArrayAlloc
 - propvarutil/VariantToUInt16ArrayAlloc
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
 - VariantToUInt16ArrayAlloc
---

# VariantToUInt16ArrayAlloc function


## -description

Extracts data from a vector structure into a newly-allocated unsigned <b>Int16</b> array.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pprgn [out]

Type: <b>USHORT**</b>

Pointer to the address of the unsigned <b>Int16</b> data extracted from the source variant structure.

### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of unsigned <b>Int16</b> elements extracted from the source variant structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

