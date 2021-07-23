---
UID: NF:intsafe.IntPtrToChar
title: IntPtrToChar function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type CHAR.
helpviewer_keywords: ["IntPtrToChar","IntPtrToChar function [Windows Shell]","intsafe/IntPtrToChar","shell.IntPtrToChar"]
old-location: shell\IntPtrToChar.htm
tech.root: shell
ms.assetid: e0f8139e-9d40-4fac-a08b-651909b0a567
ms.date: 12/05/2018
ms.keywords: IntPtrToChar, IntPtrToChar function [Windows Shell], intsafe/IntPtrToChar, shell.IntPtrToChar
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IntPtrToChar
 - intsafe/IntPtrToChar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - IntPtrToChar
---

# IntPtrToChar function


## -description

Converts a value of type <b>INT_PTR</b> to a value of type <b>CHAR</b>.

## -parameters

### -param iOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

