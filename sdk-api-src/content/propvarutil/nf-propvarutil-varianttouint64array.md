---
UID: NF:propvarutil.VariantToUInt64Array
title: VariantToUInt64Array function
author: windows-sdk-content
description: Extracts data from a vector structure into an unsigned Int64 array.
old-location: properties\VariantToUInt64Array.htm
old-project: properties
ms.assetid: 90b39ed2-a8a9-424c-bfd2-90517b9224fd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VariantToUInt64Array, VariantToUInt64Array function [Windows Properties], _shell_VariantToUInt64Array, properties.VariantToUInt64Array, propvarutil/VariantToUInt64Array, shell.VariantToUInt64Array
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToUInt64Array
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# VariantToUInt64Array function


## -description


Extracts data from a vector structure into an unsigned <b>Int64</b> array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param prgn [out]

Type: <b>ULONGLONG*</b>

Pointer to the unsigned <b>Int64</b> data extracted from source variant structure.


### -param crgn [in]

Type: <b>ULONG</b>

Specifies unsigned <b>Int64</b> array size.


### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of unsigned <b>Int64</b> elements extracted from source variant structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



