---
UID: NF:intsafe.ULongLongSub
title: ULongLongSub function (intsafe.h)
description: Subtracts one value of type SIZE_T from another.
helpviewer_keywords: ["SIZETSub","SIZETSub function [Windows Shell]","ULongLongSub","_shell_SIZETSub","intsafe/SIZETSub","shell.SIZETSub","shell.SIZETSub_1"]
old-location: shell\SIZETSub_1.htm
tech.root: shell
ms.assetid: 10c66f6a-648d-4308-9c23-384ebe273af3
ms.date: 12/05/2018
ms.keywords: SIZETSub, SIZETSub function [Windows Shell], ULongLongSub, _shell_SIZETSub, intsafe/SIZETSub, shell.SIZETSub, shell.SIZETSub_1
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
 - ULongLongSub
 - intsafe/ULongLongSub
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
 - SIZETSub
---

# ULongLongSub function


## -description

Subtracts one value of type <b>SIZE_T</b> from another.

## -parameters

### -param ullMinuend [in]

Type: <b>SIZE_T</b>

The value from which <i>cbSubtrahend</i> is subtracted.

### -param ullSubtrahend [in]

Type: <b>SIZE_T</b>

The value to subtract from <i>cbMinuend</i>.

### -param pullResult [out]

Type: <b>SIZE_T*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

