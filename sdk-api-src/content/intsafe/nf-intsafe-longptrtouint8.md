---
UID: NF:intsafe.LongPtrToUInt8
title: LongPtrToUInt8 function (intsafe.h)
description: Converts a value of type LONG_PTR to a value of type UINT8.
helpviewer_keywords: ["LongPtrToUInt8","LongPtrToUInt8 function [Windows Shell]","intsafe/LongPtrToUInt8","shell.LongPtrToUInt8"]
old-location: shell\LongPtrToUInt8.htm
tech.root: shell
ms.assetid: 001d5029-b24e-4f00-a93c-a4123bdb3021
ms.date: 12/05/2018
ms.keywords: LongPtrToUInt8, LongPtrToUInt8 function [Windows Shell], intsafe/LongPtrToUInt8, shell.LongPtrToUInt8
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
 - LongPtrToUInt8
 - intsafe/LongPtrToUInt8
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
 - LongPtrToUInt8
---

# LongPtrToUInt8 function


## -description

Converts a value of type <b>LONG_PTR</b> to a value of type <b>UINT8</b>.

## -parameters

### -param lOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

