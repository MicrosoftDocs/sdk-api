---
UID: NF:intsafe.ULongPtrToIntPtr
title: ULongPtrToIntPtr function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type INT_PTR.
helpviewer_keywords: ["DWordPtrToIntPtr","DWordPtrToPtrdiffT","SIZETToIntPtr","SIZETToPtrdiffT","ULongPtrToIntPtr","ULongPtrToIntPtr function [Windows Shell]","ULongPtrToPtrdiffT","_shell_ULongPtrToIntPtr","intsafe/ULongPtrToIntPtr","shell.ULongPtrToIntPtr"]
old-location: shell\ULongPtrToIntPtr.htm
tech.root: shell
ms.assetid: 06d85c02-8ccf-4913-aec5-f338eebdf366
ms.date: 12/05/2018
ms.keywords: DWordPtrToIntPtr, DWordPtrToPtrdiffT, SIZETToIntPtr, SIZETToPtrdiffT, ULongPtrToIntPtr, ULongPtrToIntPtr function [Windows Shell], ULongPtrToPtrdiffT, _shell_ULongPtrToIntPtr, intsafe/ULongPtrToIntPtr, shell.ULongPtrToIntPtr
f1_keywords:
- intsafe/ULongPtrToIntPtr
dev_langs:
- c++
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
- ULongPtrToIntPtr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ULongPtrToIntPtr function


## -description


Converts a value of type <b>ULONG_PTR</b> to a value of type <b>INT_PTR</b>.


## -parameters




### -param ulOperand [in]

Type: <b>ULONG_PTR</b>

The value to be converted.


### -param piResult [out]

Type: <b>INT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>DWordPtrToPtrdiffT</b> is an alias for this function.

<b>SIZETToPtrdiffT</b> is an alias for this function.

<b>SIZETToIntPtr</b> is an alias for this function.

<b>ULongPtrToPtrdiffT</b> is an alias for this function.

<b>DWordPtrToIntPtr</b> is an alias for this function.



