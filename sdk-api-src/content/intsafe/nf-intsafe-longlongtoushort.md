---
UID: NF:intsafe.LongLongToUShort
title: LongLongToUShort function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type USHORT.
helpviewer_keywords: ["LongLongToUShort","LongLongToUShort function [Windows Shell]","intsafe/LongLongToUShort","shell.LongLongToUShort"]
old-location: shell\LongLongToUShort.htm
tech.root: shell
ms.assetid: fd70ca5d-1dc0-4d2a-b497-a7df9cfba95c
ms.date: 12/05/2018
ms.keywords: LongLongToUShort, LongLongToUShort function [Windows Shell], intsafe/LongLongToUShort, shell.LongLongToUShort
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
 - LongLongToUShort
 - intsafe/LongLongToUShort
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
 - LongLongToUShort
---

# LongLongToUShort function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>USHORT</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param pusResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

