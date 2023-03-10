---
UID: NF:intsafe.ULongPtrAdd
title: ULongPtrAdd function (intsafe.h)
description: Adds two values of type ULONG_PTR.
helpviewer_keywords: ["ULongPtrAdd","ULongPtrAdd function [Windows Shell]","_shell_ULongPtrAdd","intsafe/ULongPtrAdd","shell.ULongPtrAdd"]
old-location: shell\ULongPtrAdd.htm
tech.root: shell
ms.assetid: 83f89ca7-0625-4705-9645-b2b739a9d664
ms.date: 12/05/2018
ms.keywords: ULongPtrAdd, ULongPtrAdd function [Windows Shell], _shell_ULongPtrAdd, intsafe/ULongPtrAdd, shell.ULongPtrAdd
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
 - ULongPtrAdd
 - intsafe/ULongPtrAdd
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
 - ULongPtrAdd
---

# ULongPtrAdd function


## -description

Adds two values of type <b>ULONG_PTR</b>.

## -parameters

### -param ulAugend [in]

Type: <b>ULONG_PTR</b>

The first value in the equation.

### -param ulAddend [in]

Type: <b>ULONG_PTR</b>

The value to add to <i>ulAugend</i>.

### -param pulResult [out]

Type: <b>ULONG_PTR*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

