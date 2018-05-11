---
UID: NF:propvarutil.VariantGetElementCount
title: VariantGetElementCount function
author: windows-driver-content
description: Retrieves the element count of a variant structure.
old-location: properties\VariantGetElementCount.htm
old-project: properties
ms.assetid: 2bf96650-c0c4-4c99-9a04-d36d506b8f68
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: VariantGetElementCount, VariantGetElementCount function [Windows Properties], _shell_VariantGetElementCount, properties.VariantGetElementCount, propvarutil/VariantGetElementCount, shell.VariantGetElementCount
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
-	VariantGetElementCount
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VariantGetElementCount function


## -description


Retrieves the element count of a variant structure.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


## -returns



Type: <b>ULONG</b>

Returns the element count for values of type VT_ARRAY; otherwise, returns 1.



