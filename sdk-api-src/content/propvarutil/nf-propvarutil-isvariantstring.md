---
UID: NF:propvarutil.IsVariantString
title: IsVariantString function
author: windows-driver-content
description: Specifies whether a variant is a string.
old-location: properties\IsVariantString.htm
old-project: properties
ms.assetid: 6056856c-9b7a-4c6a-9e9a-0baa5e1addcf
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IsVariantString, IsVariantString function [Windows Properties], _shell_IsVariantString, properties.IsVariantString, propvarutil/IsVariantString, shell.IsVariantString
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
-	IsVariantString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IsVariantString function


## -description


Specifies whether a variant is a string.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to the variant being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if variant is a string.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.



