---
UID: NF:propvarutil.VariantGetUInt32Elem
title: VariantGetUInt32Elem function
author: windows-sdk-content
description: Extracts a single unsigned Int32 element from a variant structure.
old-location: properties\VariantGetUInt32Elem.htm
old-project: properties
ms.assetid: b950d051-2500-4523-8307-5817274878f2
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: VariantGetUInt32Elem, VariantGetUInt32Elem function [Windows Properties], _shell_VariantGetUInt32Elem, properties.VariantGetUInt32Elem, propvarutil/VariantGetUInt32Elem, shell.VariantGetUInt32Elem
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
-	VariantGetUInt32Elem
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantGetUInt32Elem function


## -description


Extracts a single unsigned <b>Int32</b> element from a variant structure.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, value must be 0.


### -param pnVal [out]

Type: <b>ULONG*</b>

Pointer to the extracted element value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



