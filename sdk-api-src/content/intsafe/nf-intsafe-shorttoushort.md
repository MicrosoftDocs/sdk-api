---
UID: NF:intsafe.ShortToUShort
title: ShortToUShort function (intsafe.h)
description: Converts a value of type SHORT to a value of type USHORT.
helpviewer_keywords: ["ShortToUShort","ShortToUShort function [Windows Shell]","ShortToWord","_shell_ShortToUShort","intsafe/ShortToUShort","shell.ShortToUShort"]
old-location: shell\ShortToUShort.htm
tech.root: shell
ms.assetid: 35820e7f-db32-439b-a96b-8891ab2ab5ae
ms.date: 12/05/2018
ms.keywords: ShortToUShort, ShortToUShort function [Windows Shell], ShortToWord, _shell_ShortToUShort, intsafe/ShortToUShort, shell.ShortToUShort
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
 - ShortToUShort
 - intsafe/ShortToUShort
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
 - ShortToUShort
---

# ShortToUShort function


## -description

Converts a value of type <b>SHORT</b> to a value of type <b>USHORT</b>.

## -parameters

### -param sOperand [in]

Type: <b>SHORT</b>

The value to be converted.

### -param pusResult [out]

Type: <b>USHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>ShortToWord</b> is an alias for this function.

