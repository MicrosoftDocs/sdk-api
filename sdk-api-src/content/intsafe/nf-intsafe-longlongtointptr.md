---
UID: NF:intsafe.LongLongToIntPtr
title: LongLongToIntPtr function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type INT_PTR.
helpviewer_keywords: ["Int64ToIntPtr","Int64ToPtrdiffT","LongLongToIntPtr","LongLongToIntPtr function [Windows Shell]","intsafe/LongLongToIntPtr","shell.LongLongToIntPtr"]
old-location: shell\LongLongToIntPtr.htm
tech.root: shell
ms.assetid: fb10650f-6536-491c-8897-0f826b506e5a
ms.date: 12/05/2018
ms.keywords: Int64ToIntPtr, Int64ToPtrdiffT, LongLongToIntPtr, LongLongToIntPtr function [Windows Shell], intsafe/LongLongToIntPtr, shell.LongLongToIntPtr
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
 - LongLongToIntPtr
 - intsafe/LongLongToIntPtr
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
 - LongLongToIntPtr
---

# LongLongToIntPtr function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>INT_PTR</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param piResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Int64ToPtrdiffT</b> is an alias for this function.

<b>Int64ToIntPtr</b> is an alias for this function.

