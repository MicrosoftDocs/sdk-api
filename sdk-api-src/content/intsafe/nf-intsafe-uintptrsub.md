---
UID: NF:intsafe.UIntPtrSub
title: UIntPtrSub function (intsafe.h)
description: Subtracts one value of type UINT_PTR from another.
helpviewer_keywords: ["UIntPtrSub","UIntPtrSub function [Windows Shell]","_shell_UIntPtrSub","intsafe/UIntPtrSub","shell.UIntPtrSub"]
old-location: shell\UIntPtrSub.htm
tech.root: shell
ms.assetid: 629bc700-ca64-4849-bdad-59e67857ff8d
ms.date: 12/05/2018
ms.keywords: UIntPtrSub, UIntPtrSub function [Windows Shell], _shell_UIntPtrSub, intsafe/UIntPtrSub, shell.UIntPtrSub
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
 - UIntPtrSub
 - intsafe/UIntPtrSub
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
 - UIntPtrSub
---

# UIntPtrSub function


## -description

Subtracts one value of type <b>UINT_PTR</b> from another.

## -parameters

### -param uMinuend [in]

Type: <b>UINT_PTR</b>

The value from which <i>uSubtrahend</i> is subtracted.

### -param uSubtrahend [in]

Type: <b>UINT_PTR</b>

The value to subtract from <i>uMinuend</i>.

### -param puResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

