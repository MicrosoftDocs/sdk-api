---
UID: NF:intsafe.IntMult
title: IntMult function
author: windows-driver-content
description: Multiplies two values of type INT.
old-location: shell\IntMult.htm
old-project: shell
ms.assetid: 7a8ec63e-7424-4a12-9bc9-7c91e4c49fa7
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IntMult, IntMult function [Windows Shell], intsafe/IntMult, shell.IntMult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	intsafe.h
api_name:
-	IntMult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntMult function


## -description


Multiplies two values of type <b>INT</b>.


## -parameters




### -param iMultiplicand [in]

The first value.


### -param iMultiplier [in]

The second value.


### -param piResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



