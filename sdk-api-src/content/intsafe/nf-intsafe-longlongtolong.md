---
UID: NF:intsafe.LongLongToLong
title: LongLongToLong function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type LONG.
helpviewer_keywords: ["Int64ToLong","LongLongToLong","LongLongToLong function [Windows Shell]","intsafe/LongLongToLong","shell.LongLongToLong"]
old-location: shell\LongLongToLong.htm
tech.root: shell
ms.assetid: c77dbb9f-6c3a-4793-9740-ce9b75727b0d
ms.date: 12/05/2018
ms.keywords: Int64ToLong, LongLongToLong, LongLongToLong function [Windows Shell], intsafe/LongLongToLong, shell.LongLongToLong
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
 - LongLongToLong
 - intsafe/LongLongToLong
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
 - LongLongToLong
---

# LongLongToLong function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>LONG</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param plResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Int64ToLong</b> is an alias for this function.

