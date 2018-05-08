---
UID: NF:intsafe.ULongMult
title: ULongMult function
author: windows-driver-content
description: Multiplies one value of type DWORD by another.
old-location: shell\DWordMult.htm
old-project: shell
ms.assetid: 80fd88c1-b05b-468f-9dc7-c6a432e49d6d
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: DWordMult, DWordMult function [Windows Shell], ULongMult, _shell_DWordMult, intsafe/DWordMult, shell.DWordMult
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
-	DllExport
api_location:
-	None
api_name:
-	DWordMult
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongMult function


## -description


Multiplies one value of type <b>DWORD</b> by another.


## -parameters




### -param ulMultiplicand

TBD


### -param ulMultiplier

TBD


### -param pulResult

TBD




#### - dwMultiplicand [in]

Type: <b>DWORD</b>

The value to be multiplied by <i>dwMultiplier</i>.


#### - dwMultiplier [in]

Type: <b>DWORD</b>

The value by which to multiply <i>dwMultiplicand</i>.


#### - pdwResult [out]

Type: <b>DWORD*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



