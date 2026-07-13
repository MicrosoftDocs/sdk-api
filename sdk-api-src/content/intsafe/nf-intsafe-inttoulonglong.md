---
UID: NF:intsafe.IntToULongLong
title: IntToULongLong function (intsafe.h)
description: Converts a value of type INT to a value of type UINT_PTR.
helpviewer_keywords: ["IntToUIntPtr","IntToUIntPtr function [Windows Shell]","IntToULongLong","_shell_IntToUIntPtr","intsafe/IntToUIntPtr","shell.IntToUIntPtr"]
old-location: shell\IntToUIntPtr.htm
tech.root: shell
ms.assetid: 479958f6-e38c-404c-b4bd-2991be568a2b
ms.date: 12/05/2018
ms.keywords: IntToUIntPtr, IntToUIntPtr function [Windows Shell], IntToULongLong, _shell_IntToUIntPtr, intsafe/IntToUIntPtr, shell.IntToUIntPtr
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
 - IntToULongLong
 - intsafe/IntToULongLong
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
 - IntToUIntPtr
---

# IntToULongLong function


## -description

Converts a value of type <b>INT</b> to a value of type <b>UINT_PTR</b>.

## -parameters

### -param iOperand [in]

Type: <b>INT</b>

The value to be converted.

### -param pullResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the address of the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

