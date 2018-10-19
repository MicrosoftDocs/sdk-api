---
UID: NF:intsafe.UIntPtrToIntPtr
title: UIntPtrToIntPtr function
author: windows-sdk-content
description: Converts a value of type UINT_PTR to a value of type INT_PTR.
old-location: shell\UIntPtrToIntPtr.htm
tech.root: shell
ms.assetid: c922b108-47af-46fe-9753-66cad96ec352
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: SizeTToIntPtr, SizeTToPtrdiffT, UIntPtrToIntPtr, UIntPtrToIntPtr function [Windows Shell], _shell_UIntPtrToIntPtr, intsafe/UIntPtrToIntPtr, shell.UIntPtrToIntPtr
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - UIntPtrToIntPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UIntPtrToIntPtr function


## -description


Converts a value of type <b>UINT_PTR</b> to a value of type <b>INT_PTR</b>.


## -parameters




### -param uOperand [in]

Type: <b>UINT_PTR</b>

The value to be converted.


### -param piResult [out]

Type: <b>INT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>SizeTToPtrdiffT</b> is an alias for this function.

<b>SizeTToIntPtr</b> is an alias for this function.



