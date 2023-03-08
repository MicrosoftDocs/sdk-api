---
UID: NF:intsafe.ULongLongToUIntPtr
title: ULongLongToUIntPtr function (intsafe.h)
description: Converts a value of type ULONGLONG to a value of type UINT_PTR.
helpviewer_keywords: ["ULongLongToSizeT","ULongLongToUIntPtr","ULongLongToUIntPtr function [Windows Shell]","_shell_ULongLongToUIntPtr","intsafe/ULongLongToUIntPtr","shell.ULongLongToUIntPtr"]
old-location: shell\ULongLongToUIntPtr.htm
tech.root: shell
ms.assetid: c3c08ff3-e583-435d-9e44-5fab9371b7cd
ms.date: 12/05/2018
ms.keywords: ULongLongToSizeT, ULongLongToUIntPtr, ULongLongToUIntPtr function [Windows Shell], _shell_ULongLongToUIntPtr, intsafe/ULongLongToUIntPtr, shell.ULongLongToUIntPtr
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
 - ULongLongToUIntPtr
 - intsafe/ULongLongToUIntPtr
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
 - ULongLongToUIntPtr
---

# ULongLongToUIntPtr function


## -description

Converts a value of type <b>ULONGLONG</b> to a value of type <b>UINT_PTR</b>.

## -parameters

### -param ullOperand [in]

Type: <b>ULONGLONG</b>

The value to be converted.

### -param puResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>ULongLongToSizeT</b> is an alias for this function.

