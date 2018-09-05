---
UID: NF:intsafe.UIntPtrMult
title: UIntPtrMult function
author: windows-sdk-content
description: Multiplies one value of type UINT_PTR by another.
old-location: shell\UIntPtrMult.htm
old-project: shell
ms.assetid: c34708d1-50e8-47dd-ac79-cfef24ce6060
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: UIntPtrMult, UIntPtrMult function [Windows Shell], _shell_UIntPtrMult, intsafe/UIntPtrMult, shell.UIntPtrMult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.redist: 
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
 - UIntPtrMult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrMult function


## -description


Multiplies one value of type <b>UINT_PTR</b> by another.


## -parameters




### -param uMultiplicand [in]

Type: <b>UINT_PTR</b>

The value to be multiplied by <i>uMultiplier</i>.


### -param uMultiplier [in]

Type: <b>UINT_PTR</b>

The value by which to multiply <i>uMultiplicand</i>.


### -param puResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



