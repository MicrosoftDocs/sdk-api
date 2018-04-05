---
UID: NF:intsafe.ULongLongMult
title: ULongLongMult function
author: windows-driver-content
description: Multiplies one value of type ULONGLONG by another.
old-location: shell\ULongLongMult.htm
old-project: shell
ms.assetid: 69033eba-a0ad-4c76-b1c5-2cbd412e9f9c
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ULongLongMult, ULongLongMult function [Windows Shell], _shell_ULongLongMult, intsafe/ULongLongMult, shell.ULongLongMult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	Intsafe.h
api_name:
-	ULongLongMult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongMult function


## -description


Multiplies one value of type <b>ULONGLONG</b> by another.


## -parameters




### -param ullMultiplicand [in]

Type: <b>ULONGLONG</b>

The value to be multiplied by <i>ullMultiplier</i>.


### -param ullMultiplier [in]

Type: <b>ULONGLONG</b>

The value by which to multiply <i>ullMultiplicand</i>.


### -param pullResult [out]

Type: <b>ULONGLONG*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



