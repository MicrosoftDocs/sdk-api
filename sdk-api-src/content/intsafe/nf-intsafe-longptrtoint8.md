---
UID: NF:intsafe.LongPtrToInt8
title: LongPtrToInt8 function (intsafe.h)
description: Converts a value of type LONG_PTR to a value of type INT8.
helpviewer_keywords: ["LongPtrToInt8","LongPtrToInt8 function [Windows Shell]","intsafe/LongPtrToInt8","shell.LongPtrToInt8"]
old-location: shell\LongPtrToInt8.htm
tech.root: shell
ms.assetid: 38ef67b9-362f-4776-9b4c-6ca40e1efe0b
ms.date: 12/05/2018
ms.keywords: LongPtrToInt8, LongPtrToInt8 function [Windows Shell], intsafe/LongPtrToInt8, shell.LongPtrToInt8
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
 - LongPtrToInt8
 - intsafe/LongPtrToInt8
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
 - LongPtrToInt8
---

# LongPtrToInt8 function


## -description

Converts a value of type <b>LONG_PTR</b> to a value of type <b>INT8</b>.

## -parameters

### -param lOperand [in]

The value to convert.

### -param pi8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

