---
UID: NF:intsafe.IntToShort
title: IntToShort function (intsafe.h)
description: Converts a value of type INT to a value of type SHORT.
helpviewer_keywords: ["IntToShort","IntToShort function [Windows Shell]","_shell_IntToShort","intsafe/IntToShort","shell.IntToShort"]
old-location: shell\IntToShort.htm
tech.root: shell
ms.assetid: a3f6ae04-fa81-4b41-9792-5e3403016f1d
ms.date: 12/05/2018
ms.keywords: IntToShort, IntToShort function [Windows Shell], _shell_IntToShort, intsafe/IntToShort, shell.IntToShort
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
 - IntToShort
 - intsafe/IntToShort
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
 - IntToShort
---

# IntToShort function


## -description

Converts a value of type <b>INT</b> to a value of type <b>SHORT</b>.

## -parameters

### -param iOperand [in]

Type: <b>INT</b>

The value to be converted.

### -param psResult [out]

Type: <b>SHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

