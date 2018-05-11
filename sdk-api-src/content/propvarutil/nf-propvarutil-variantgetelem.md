---
UID: NF:propvarutil.VariantGetElem
title: VariantGetElem function
author: windows-driver-content
description: Initializes a VARIANT structure from a specified variant element.
old-location: properties\VariantGetElem.htm
old-project: properties
ms.assetid: e1541e66-3ccc-494c-a909-72eeb9159d11
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: VariantGetElem, VariantGetElem function [Windows Properties], _shell_VariantGetElem, properties.VariantGetElem, propvarutil/VariantGetElem, shell.VariantGetElem
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
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	VariantGetElem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VariantGetElem function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure from a specified variant element.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies index of source variant structure element. If source structure is empty, then this parameter is not used.


### -param pvar [out]

Type: <b>VARIANT*</b>

Pointer to the values specified from the source variant structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.



