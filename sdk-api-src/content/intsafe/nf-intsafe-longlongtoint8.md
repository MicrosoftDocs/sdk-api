---
UID: NF:intsafe.LongLongToInt8
title: LongLongToInt8 function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type INT8.
helpviewer_keywords: ["LongLongToInt8","LongLongToInt8 function [Windows Shell]","intsafe/LongLongToInt8","shell.LongLongToInt8"]
old-location: shell\LongLongToInt8.htm
tech.root: shell
ms.assetid: 6250ae35-5422-4220-a45c-5569854d051c
ms.date: 12/05/2018
ms.keywords: LongLongToInt8, LongLongToInt8 function [Windows Shell], intsafe/LongLongToInt8, shell.LongLongToInt8
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
 - LongLongToInt8
 - intsafe/LongLongToInt8
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
 - LongLongToInt8
---

# LongLongToInt8 function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>INT8</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param pi8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

