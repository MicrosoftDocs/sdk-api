---
UID: NF:intsafe.LongLongToUInt
title: LongLongToUInt function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type UINT.
helpviewer_keywords: ["Int64ToSizeT","Int64ToUInt","Int64ToUIntPtr","Int64ToULongPtr","LongLongToUInt","LongLongToUInt function [Windows Shell]","intsafe/LongLongToUInt","shell.LongLongToUInt"]
old-location: shell\LongLongToUInt.htm
tech.root: shell
ms.assetid: e9bb0a51-3593-4074-8ea1-10fb9f0d8087
ms.date: 12/05/2018
ms.keywords: Int64ToSizeT, Int64ToUInt, Int64ToUIntPtr, Int64ToULongPtr, LongLongToUInt, LongLongToUInt function [Windows Shell], intsafe/LongLongToUInt, shell.LongLongToUInt
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
 - LongLongToUInt
 - intsafe/LongLongToUInt
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
 - LongLongToUInt
---

# LongLongToUInt function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>UINT</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param puResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Int64ToULongPtr</b> is an alias for this function.

<b>Int64ToUIntPtr</b> is an alias for this function.

<b>Int64ToUInt</b> is an alias for this function.

<b>Int64ToSizeT</b> is an alias for this function.

