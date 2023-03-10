---
UID: NF:intsafe.ULongPtrToInt
title: ULongPtrToInt function (intsafe.h)
description: Converts a value of type size_t to a value of type INT.
helpviewer_keywords: ["SizeTToInt","SizeTToInt function [Windows Shell]","ULongPtrToInt","_shell_SizeTToInt","intsafe/SizeTToInt","shell.SizeTToInt"]
old-location: shell\SizeTToInt.htm
tech.root: shell
ms.assetid: 65f178c1-8029-40c5-af31-03f158d90582
ms.date: 12/05/2018
ms.keywords: SizeTToInt, SizeTToInt function [Windows Shell], ULongPtrToInt, _shell_SizeTToInt, intsafe/SizeTToInt, shell.SizeTToInt
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
 - ULongPtrToInt
 - intsafe/ULongPtrToInt
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
 - SizeTToInt
---

# ULongPtrToInt function


## -description

Converts a value of type <b>size_t</b> to a value of type <b>INT</b>.

## -parameters

### -param ulOperand [in]

Type: <b>size_t</b>

The value to be converted.

### -param piResult [out]

Type: <b>INT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

