---
UID: NF:propvarutil.VariantToInt16
title: VariantToInt16 function
author: windows-driver-content
description: Extracts the Int16 property value of a variant structure. If no value can be extracted, then a default value is assigned by this function.
old-location: properties\VariantToInt16.htm
old-project: properties
ms.assetid: 5a0d22c1-4295-405d-a503-2b9fdd6eaa81
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: VariantToInt16, VariantToInt16 function [Windows Properties], _shell_VariantToInt16, properties.VariantToInt16, propvarutil/VariantToInt16, shell.VariantToInt16
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
-	VariantToInt16
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VariantToInt16 function


## -description


Extracts the <b>Int16</b> property value of a variant structure. If no value can be extracted, then a default value is assigned by this function.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param piRet [out]

Type: <b>SHORT*</b>

Pointer to the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



