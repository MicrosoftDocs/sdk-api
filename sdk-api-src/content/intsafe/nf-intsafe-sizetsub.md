---
UID: NF:intsafe.SizeTSub
title: SizeTSub function (intsafe.h)
description: Subtracts one value of type size_t from another.
helpviewer_keywords: ["SizeTSub","SizeTSub function [Windows Shell]","_shell_SizeTSub","intsafe/SizeTSub","shell.SizeTSub"]
old-location: shell\SizeTSub.htm
tech.root: shell
ms.assetid: 6a7b22e7-504b-4065-80fa-b972f0360b5c
ms.date: 12/05/2018
ms.keywords: SizeTSub, SizeTSub function [Windows Shell], _shell_SizeTSub, intsafe/SizeTSub, shell.SizeTSub
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
 - SizeTSub
 - intsafe/SizeTSub
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
 - SizeTSub
---

# SizeTSub function


## -description

Subtracts one value of type <b>size_t</b> from another.

## -parameters

### -param Minuend [in]

Type: <b>size_t</b>

The value from which <i>cbSubtrahend</i> is subtracted.

### -param Subtrahend [in]

Type: <b>size_t</b>

The value to subtract from <i>cbMinuend</i>.

### -param pResult [out]

Type: <b>size_t*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

