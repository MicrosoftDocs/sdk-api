---
UID: NF:intsafe.UIntPtrAdd
title: UIntPtrAdd function (intsafe.h)
description: Adds two values of type UINT_PTR.
helpviewer_keywords: ["UIntPtrAdd","UIntPtrAdd function [Windows Shell]","_shell_UIntPtrAdd","intsafe/UIntPtrAdd","shell.UIntPtrAdd"]
old-location: shell\UIntPtrAdd.htm
tech.root: shell
ms.assetid: 85658194-cb13-443f-8e6b-84034f7cd46b
ms.date: 12/05/2018
ms.keywords: UIntPtrAdd, UIntPtrAdd function [Windows Shell], _shell_UIntPtrAdd, intsafe/UIntPtrAdd, shell.UIntPtrAdd
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
 - UIntPtrAdd
 - intsafe/UIntPtrAdd
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
 - UIntPtrAdd
---

# UIntPtrAdd function


## -description

Adds two values of type <b>UINT_PTR</b>.

## -parameters

### -param uAugend [in]

Type: <b>UINT_PTR</b>

The first value in the equation.

### -param uAddend [in]

Type: <b>UINT_PTR</b>

The value to add to <i>uAugend</i>.

### -param puResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

