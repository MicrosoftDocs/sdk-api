---
UID: NF:intsafe.ULongLongMult
title: ULongLongMult function (intsafe.h)
description: Multiplies one value of type size_t by another.S
helpviewer_keywords: ["SizeTMult","SizeTMult function [Windows Shell]","ULongLongMult","_shell_SizeTMult","intsafe/SizeTMult","shell.SizeTMult"]
old-location: shell\SizeTMult.htm
tech.root: shell
ms.assetid: 078bc77b-6af3-4d13-8f98-5f52605fdf8d
ms.date: 12/05/2018
ms.keywords: SizeTMult, SizeTMult function [Windows Shell], ULongLongMult, _shell_SizeTMult, intsafe/SizeTMult, shell.SizeTMult
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
 - ULongLongMult
 - intsafe/ULongLongMult
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
 - SizeTMult
---

## -description

Multiplies one value of type <b>size_t</b> by another.

## -parameters

### -param ullMultiplicand [in]

The value to be multiplied by <i>cbMultiplier</i>.

### -param ullMultiplier [in]

The value by which to multiply <i>cbMultiplicand</i>.

### -param pullResult [out]

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.
