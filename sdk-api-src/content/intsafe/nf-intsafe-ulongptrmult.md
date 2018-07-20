---
UID: NF:intsafe.ULongPtrMult
title: ULongPtrMult function
author: windows-sdk-content
description: Multiplies one value of type ULONG_PTR by another.
old-location: shell\ULongPtrMult.htm
old-project: shell
ms.assetid: e3ee5794-b872-4286-b4f3-1c5cab0e42a8
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ULongPtrMult, ULongPtrMult function [Windows Shell], _shell_ULongPtrMult, intsafe/ULongPtrMult, shell.ULongPtrMult
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - ULongPtrMult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongPtrMult function


## -description


Multiplies one value of type <b>ULONG_PTR</b> by another.


## -parameters




### -param ulMultiplicand [in]

Type: <b>ULONG_PTR</b>

The value to be multiplied by <i>ulMultiplier</i>.


### -param ulMultiplier [in]

Type: <b>ULONG_PTR</b>

The value by which to multiply <i>ulMultiplicand</i>.


### -param pulResult [out]

Type: <b>ULONG_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



