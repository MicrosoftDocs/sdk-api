---
UID: NF:intsafe.ULongPtrSub
title: ULongPtrSub function (intsafe.h)
description: Subtracts one value of type ULONG_PTR from another.
helpviewer_keywords: ["ULongPtrSub","ULongPtrSub function [Windows Shell]","_shell_ULongPtrSub","intsafe/ULongPtrSub","shell.ULongPtrSub"]
old-location: shell\ULongPtrSub.htm
tech.root: shell
ms.assetid: 29cc4dec-e02d-4ce4-a615-9b62bd08befb
ms.date: 12/05/2018
ms.keywords: ULongPtrSub, ULongPtrSub function [Windows Shell], _shell_ULongPtrSub, intsafe/ULongPtrSub, shell.ULongPtrSub
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ULongPtrSub
 - intsafe/ULongPtrSub
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - ULongPtrSub
---

# ULongPtrSub function


## -description

Subtracts one value of type <b>ULONG_PTR</b> from another.

## -parameters

### -param ulMinuend [in]

Type: <b>ULONG_PTR</b>

The value from which <i>ulSubtrahend</i> is subtracted.

### -param ulSubtrahend [in]

Type: <b>ULONG_PTR</b>

The value to subtract from <i>ulMinuend</i>.

### -param pulResult [out]

Type: <b>ULONG_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks, and to do so with minimal impact on performance.

