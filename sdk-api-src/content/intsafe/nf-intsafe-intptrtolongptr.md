---
UID: NF:intsafe.IntPtrToLongPtr
title: IntPtrToLongPtr function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type LONG_PTR.
helpviewer_keywords: ["IntPtrToLongPtr","IntPtrToLongPtr function [Windows Shell]","intsafe/IntPtrToLongPtr","shell.IntPtrToLongPtr"]
old-location: shell\IntPtrToLongPtr.htm
tech.root: shell
ms.assetid: f0e4d121-9cc5-4fc9-a507-b9fc8e314f94
ms.date: 12/05/2018
ms.keywords: IntPtrToLongPtr, IntPtrToLongPtr function [Windows Shell], intsafe/IntPtrToLongPtr, shell.IntPtrToLongPtr
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
 - IntPtrToLongPtr
 - intsafe/IntPtrToLongPtr
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
 - IntPtrToLongPtr
---

# IntPtrToLongPtr function


## -description

Converts a value of type <b>INT_PTR</b> to a value of type <b>LONG_PTR</b>.

## -parameters

### -param iOperand [in]

The value to convert.

### -param plResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

