---
UID: NF:intsafe.ULongAdd
title: ULongAdd function
author: windows-driver-content
description: Adds two values of type ULONG.
old-location: shell\ULongAdd.htm
old-project: shell
ms.assetid: 63726f12-ba01-4cb7-a311-95d476e68174
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DWordAdd, ULongAdd, ULongAdd function [Windows Shell], _shell_ULongAdd, intsafe/ULongAdd, shell.ULongAdd
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
-	ULongAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongAdd function


## -description


Adds two values of type <b>ULONG</b>.


## -parameters




### -param ulAugend [in]

Type: <b>ULONG</b>

The first value in the equation.


### -param ulAddend [in]

Type: <b>ULONG</b>

The value to add to <i>ulAugend</i>.


### -param pulResult [out]

Type: <b>ULONG*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

<b>DWordAdd</b> is an alias for this function.



