---
UID: NF:propvarutil.VariantGetInt64Elem
title: VariantGetInt64Elem function
author: windows-driver-content
description: Extracts a single Int64 element from a variant structure.
old-location: properties\VariantGetInt64Elem.htm
old-project: properties
ms.assetid: 285705d3-3b8e-40ad-abf2-1adc5adda3d8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: VariantGetInt64Elem, VariantGetInt64Elem function [Windows Properties], _shell_VariantGetInt64Elem, properties.VariantGetInt64Elem, propvarutil/VariantGetInt64Elem, shell.VariantGetInt64Elem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantGetInt64Elem
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# VariantGetInt64Elem function


## -description


Extracts a single <b>Int64</b> element from a variant structure.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, value must be 0.


### -param pnVal [out]

Type: <b>LONGLONG*</b>

Pointer to the extracted element value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



