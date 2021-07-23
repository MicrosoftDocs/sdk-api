---
UID: NF:intsafe.LongLongToUChar
title: LongLongToUChar function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type UCHAR.
helpviewer_keywords: ["LongLongToUChar","LongLongToUChar function [Windows Shell]","intsafe/LongLongToUChar","shell.LongLongToUChar"]
old-location: shell\LongLongToUChar.htm
tech.root: shell
ms.assetid: 5c8440fa-aefe-4f63-877c-4b1ebdc59138
ms.date: 12/05/2018
ms.keywords: LongLongToUChar, LongLongToUChar function [Windows Shell], intsafe/LongLongToUChar, shell.LongLongToUChar
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
 - LongLongToUChar
 - intsafe/LongLongToUChar
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
 - LongLongToUChar
---

# LongLongToUChar function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>UCHAR</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

