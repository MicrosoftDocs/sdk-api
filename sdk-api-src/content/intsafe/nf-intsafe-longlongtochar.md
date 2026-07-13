---
UID: NF:intsafe.LongLongToChar
title: LongLongToChar function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type CHAR.
helpviewer_keywords: ["LongLongToChar","LongLongToChar function [Windows Shell]","intsafe/LongLongToChar","shell.LongLongToChar"]
old-location: shell\LongLongToChar.htm
tech.root: shell
ms.assetid: c76efb04-4211-467c-8eff-d0648c426784
ms.date: 12/05/2018
ms.keywords: LongLongToChar, LongLongToChar function [Windows Shell], intsafe/LongLongToChar, shell.LongLongToChar
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
 - LongLongToChar
 - intsafe/LongLongToChar
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
 - LongLongToChar
---

# LongLongToChar function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>CHAR</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

