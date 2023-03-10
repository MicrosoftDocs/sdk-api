---
UID: NF:intsafe.LongLongToLongPtr
title: LongLongToLongPtr function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type LONG_PTR.
helpviewer_keywords: ["Int64ToLongPtr","Int64ToSSIZET","Int64ToULongPtr","LongLongToLongPtr","LongLongToLongPtr function [Windows Shell]","intsafe/LongLongToLongPtr","shell.LongLongToLongPtr"]
old-location: shell\LongLongToLongPtr.htm
tech.root: shell
ms.assetid: adda2fcd-2589-4506-a147-b2d32d7fbd69
ms.date: 12/05/2018
ms.keywords: Int64ToLongPtr, Int64ToSSIZET, Int64ToULongPtr, LongLongToLongPtr, LongLongToLongPtr function [Windows Shell], intsafe/LongLongToLongPtr, shell.LongLongToLongPtr
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
 - LongLongToLongPtr
 - intsafe/LongLongToLongPtr
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
 - LongLongToLongPtr
---

# LongLongToLongPtr function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>LONG_PTR</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param plResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Int64ToSSIZET</b> is an alias for this function.

<b>Int64ToULongPtr</b> is an alias for this function.

<b>Int64ToLongPtr</b> is an alias for this function.

