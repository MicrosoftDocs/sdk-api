---
UID: NF:propvarutil.VariantToUInt32ArrayAlloc
title: VariantToUInt32ArrayAlloc function
author: windows-sdk-content
description: Extracts data from a vector structure into a newly-allocated unsigned Int32 array.
old-location: properties\VariantToUInt32ArrayAlloc.htm
old-project: properties
ms.assetid: 4d6cbfc8-fe1c-4bd0-8d29-32bce01d31f8
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: VariantToUInt32ArrayAlloc, VariantToUInt32ArrayAlloc function [Windows Properties], _shell_VariantToUInt32ArrayAlloc, properties.VariantToUInt32ArrayAlloc, propvarutil/VariantToUInt32ArrayAlloc, shell.VariantToUInt32ArrayAlloc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantToUInt32ArrayAlloc
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantToUInt32ArrayAlloc function


## -description


Extracts data from a vector structure into a newly-allocated unsigned <b>Int32</b> array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param pprgn [out]

Type: <b>ULONG**</b>

The address of a pointer to the unsigned <b>Int32</b> data extracted from source variant structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of unsigned <b>Int32</b> elements extracted from source variant structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



