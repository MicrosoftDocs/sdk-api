---
UID: NF:intsafe.LongLongToULongLong
title: LongLongToULongLong function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type ULONGLONG.
helpviewer_keywords: ["Int64ToULongLong","IntPtrToUIntPtr","IntPtrToULongPtr","LongLongToULongLong","LongLongToULongLong function [Windows Shell]","intsafe/LongLongToULongLong","shell.LongLongToULongLong"]
old-location: shell\LongLongToULongLong.htm
tech.root: shell
ms.assetid: 994f0b9f-77a6-41ef-9022-a26ef5660204
ms.date: 12/05/2018
ms.keywords: Int64ToULongLong, IntPtrToUIntPtr, IntPtrToULongPtr, LongLongToULongLong, LongLongToULongLong function [Windows Shell], intsafe/LongLongToULongLong, shell.LongLongToULongLong
f1_keywords:
- intsafe/LongLongToULongLong
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- intsafe.h
api_name:
- LongLongToULongLong
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LongLongToULongLong function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>ULONGLONG</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param pullResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IntPtrToULongPtr</b> is an alias for this function.

<b>IntPtrToUIntPtr</b> is an alias for this function.

<b>Int64ToULongLong</b> is an alias for this function.



