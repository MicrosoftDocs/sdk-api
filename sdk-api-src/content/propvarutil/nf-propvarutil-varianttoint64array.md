---
UID: NF:propvarutil.VariantToInt64Array
title: VariantToInt64Array function
author: windows-sdk-content
description: Extracts data from a vector structure into an Int64 array.
old-location: properties\VariantToInt64Array.htm
old-project: properties
ms.assetid: 936e87e8-8102-4da2-b388-147fab6ec16f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VariantToInt64Array, VariantToInt64Array function [Windows Properties], _shell_VariantToInt64Array, properties.VariantToInt64Array, propvarutil/VariantToInt64Array, shell.VariantToInt64Array
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
 - VariantToInt64Array
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# VariantToInt64Array function


## -description


Extracts data from a vector structure into an <b>Int64</b> array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param prgn [out]

Type: <b>LONGLONG*</b>

Pointer to the Int64 data extracted from source variant structure.


### -param crgn [in]

Type: <b>ULONG</b>

Specifies Int64 array size.


### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of Int64 elements extracted from source variant structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



