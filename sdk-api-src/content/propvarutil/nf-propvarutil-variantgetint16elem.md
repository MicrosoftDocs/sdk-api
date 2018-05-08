---
UID: NF:propvarutil.VariantGetInt16Elem
title: VariantGetInt16Elem function
author: windows-driver-content
description: Extracts a single Int16 element from a variant structure.
old-location: properties\VariantGetInt16Elem.htm
old-project: properties
ms.assetid: fd572a65-c74c-490e-8cff-aa9ba54da5a1
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: VariantGetInt16Elem, VariantGetInt16Elem function [Windows Properties], _shell_VariantGetInt16Elem, properties.VariantGetInt16Elem, propvarutil/VariantGetInt16Elem, shell.VariantGetInt16Elem
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
-	VariantGetInt16Elem
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VariantGetInt16Elem function


## -description


Extracts a single <b>Int16</b> element from a variant structure.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, value must be 0.


### -param pnVal [out]

Type: <b>SHORT*</b>

Pointer to the extracted element value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



