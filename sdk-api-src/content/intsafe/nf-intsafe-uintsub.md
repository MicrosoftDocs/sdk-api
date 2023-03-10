---
UID: NF:intsafe.UIntSub
title: UIntSub function (intsafe.h)
description: Subtracts one value of type UINT from another.
helpviewer_keywords: ["UIntSub","UIntSub function [Windows Shell]","_shell_UIntSub","intsafe/UIntSub","shell.UIntSub"]
old-location: shell\UIntSub.htm
tech.root: shell
ms.assetid: be257075-84c9-40e2-af3f-75dccd97bab1
ms.date: 12/05/2018
ms.keywords: UIntSub, UIntSub function [Windows Shell], _shell_UIntSub, intsafe/UIntSub, shell.UIntSub
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
 - UIntSub
 - intsafe/UIntSub
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
 - UIntSub
---

# UIntSub function


## -description

Subtracts one value of type <b>UINT</b> from another.

## -parameters

### -param uMinuend [in]

Type: <b>UINT</b>

The value from which <i>uSubtrahend</i> is subtracted.

### -param uSubtrahend [in]

Type: <b>UINT</b>

The value to subtract from <i>uMinuend</i>.

### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

