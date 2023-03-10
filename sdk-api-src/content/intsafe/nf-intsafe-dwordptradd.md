---
UID: NF:intsafe.DWordPtrAdd
title: DWordPtrAdd function (intsafe.h)
description: Adds two values of type DWORD_PTR.
helpviewer_keywords: ["DWordPtrAdd","DWordPtrAdd function [Windows Shell]","_shell_DWordPtrAdd","intsafe/DWordPtrAdd","shell.DWordPtrAdd"]
old-location: shell\DWordPtrAdd.htm
tech.root: shell
ms.assetid: b7d2b04b-6ef7-45a5-a26c-b52c0a848d5a
ms.date: 12/05/2018
ms.keywords: DWordPtrAdd, DWordPtrAdd function [Windows Shell], _shell_DWordPtrAdd, intsafe/DWordPtrAdd, shell.DWordPtrAdd
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
req.dll: None
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWordPtrAdd
 - intsafe/DWordPtrAdd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - DWordPtrAdd
---

# DWordPtrAdd function


## -description

Adds two values of type <b>DWORD_PTR</b>.

## -parameters

### -param dwAugend [in]

Type: <b>DWORD_PTR</b>

The first value in the equation.

### -param dwAddend [in]

Type: <b>DWORD_PTR</b>

The value to add to <i>dwAugend</i>.

### -param pdwResult [out]

Type: <b>DWORD_PTR*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

