---
UID: NF:intsafe.SizeTAdd
title: SizeTAdd function (intsafe.h)
description: Adds two values of type size_t.
helpviewer_keywords: ["SizeTAdd","SizeTAdd function [Windows Shell]","_shell_SizeTAdd","intsafe/SizeTAdd","shell.SizeTAdd"]
old-location: shell\SizeTAdd.htm
tech.root: shell
ms.assetid: 1cabc944-0819-4a24-ab61-6d5375ba1573
ms.date: 12/05/2018
ms.keywords: SizeTAdd, SizeTAdd function [Windows Shell], _shell_SizeTAdd, intsafe/SizeTAdd, shell.SizeTAdd
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
 - SizeTAdd
 - intsafe/SizeTAdd
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
 - SizeTAdd
---

# SizeTAdd function


## -description

Adds two values of type <b>size_t</b>.

## -parameters

### -param Augend [in]

Type: <b>size_t</b>

The first value in the equation.

### -param Addend [in]

Type: <b>size_t</b>

The value to add to <i>cbAugend</i>.

### -param pResult [out]

Type: <b>size_t*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

