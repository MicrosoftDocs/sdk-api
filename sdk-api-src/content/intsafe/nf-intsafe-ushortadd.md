---
UID: NF:intsafe.UShortAdd
title: UShortAdd function (intsafe.h)
description: Adds two values of type USHORT.
helpviewer_keywords: ["UShortAdd","UShortAdd function [Windows Shell]","WordAdd","_shell_UShortAdd","intsafe/UShortAdd","shell.UShortAdd"]
old-location: shell\UShortAdd.htm
tech.root: shell
ms.assetid: 3aea6f4b-280f-43a1-8104-222d8f9d92cc
ms.date: 12/05/2018
ms.keywords: UShortAdd, UShortAdd function [Windows Shell], WordAdd, _shell_UShortAdd, intsafe/UShortAdd, shell.UShortAdd
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
 - UShortAdd
 - intsafe/UShortAdd
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
 - UShortAdd
---

# UShortAdd function


## -description

Adds two values of type <b>USHORT</b>.

## -parameters

### -param usAugend [in]

Type: <b>USHORT</b>

The first value in the equation.

### -param usAddend [in]

Type: <b>USHORT</b>

The value to add to <i>usAugend</i>.

### -param pusResult [out]

Type: <b>USHORT*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.

<b>WordAdd</b> is an alias for this function.

