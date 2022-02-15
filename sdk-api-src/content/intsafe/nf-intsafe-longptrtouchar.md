---
UID: NF:intsafe.LongPtrToUChar
title: LongPtrToUChar function (intsafe.h)
description: Converts a value of type LONG_PTR to a value of type UCHAR.
helpviewer_keywords: ["LongPtrToUChar","LongPtrToUChar function [Windows Shell]","intsafe/LongPtrToUChar","shell.LongPtrToUChar"]
old-location: shell\LongPtrToUChar.htm
tech.root: shell
ms.assetid: f509120e-3cb4-4696-b68b-4304155eff3b
ms.date: 12/05/2018
ms.keywords: LongPtrToUChar, LongPtrToUChar function [Windows Shell], intsafe/LongPtrToUChar, shell.LongPtrToUChar
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
 - LongPtrToUChar
 - intsafe/LongPtrToUChar
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
 - LongPtrToUChar
---

# LongPtrToUChar function


## -description

Converts a value of type <b>LONG_PTR</b> to a value of type <b>UCHAR</b>.

## -parameters

### -param lOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

