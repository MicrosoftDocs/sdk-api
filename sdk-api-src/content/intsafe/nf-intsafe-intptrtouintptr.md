---
UID: NF:intsafe.IntPtrToUIntPtr
title: IntPtrToUIntPtr function
author: windows-sdk-content
description: Converts a value of type INT_PTR to a value of type UINT_PTR.
old-location: shell\IntPtrToUIntPtr.htm
old-project: shell
ms.assetid: 9c85af51-5f28-445d-a6fe-4d3dd5666b6f
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IntPtrToSizeT, IntPtrToUIntPtr, IntPtrToUIntPtr function [Windows Shell], PtrdiffTToSizeT, PtrdiffTToUIntPtr, _shell_IntPtrToUIntPtr, intsafe/IntPtrToUIntPtr, shell.IntPtrToUIntPtr
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
 - IntPtrToUIntPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntPtrToUIntPtr function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>UINT_PTR</b>.


## -parameters




### -param iOperand [in]

Type: <b>INT_PTR</b>

A pointer to the value to be converted.


### -param puResult [out]

Type: <b>UINT_PTR*</b>

The address of the pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>PtrdiffTToUIntPtr</b> is an alias for this function.

<b>PtrdiffTToSizeT</b> is an alias for this function.

<b>IntPtrToSizeT</b> is an alias for this function.



