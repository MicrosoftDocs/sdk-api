---
UID: NF:propvarutil.VariantToInt32ArrayAlloc
title: VariantToInt32ArrayAlloc function (propvarutil.h)
author: windows-sdk-content
description: Extracts data from a vector structure into a newly-allocated Int32 array.
old-location: properties\VariantToInt32ArrayAlloc.htm
tech.root: properties
ms.assetid: 6010ee34-d7d2-4b8b-a49b-0f2aa88a3b54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VariantToInt32ArrayAlloc, VariantToInt32ArrayAlloc function [Windows Properties], _shell_VariantToInt32ArrayAlloc, properties.VariantToInt32ArrayAlloc, propvarutil/VariantToInt32ArrayAlloc, shell.VariantToInt32ArrayAlloc
ms.topic: function
f1_keywords: 
 - "propvarutil/VariantToInt32ArrayAlloc"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToInt32ArrayAlloc
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# VariantToInt32ArrayAlloc function


## -description


Extracts data from a vector structure into a newly-allocated <b>Int32</b> array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param pprgn [out]

Type: <b>LONG**</b>

Pointer to the address of the <b>Int32</b> data extracted from source variant structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of <b>Int32</b> elements extracted from source variant structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



