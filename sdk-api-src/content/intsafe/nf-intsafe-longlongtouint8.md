---
UID: NF:intsafe.LongLongToUInt8
title: LongLongToUInt8 function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type UINT8.
helpviewer_keywords: ["LongLongToUInt8","LongLongToUInt8 function [Windows Shell]","intsafe/LongLongToUInt8","shell.LongLongToUInt8"]
old-location: shell\LongLongToUInt8.htm
tech.root: shell
ms.assetid: b8dd8478-7c15-4183-9531-dd06ea2ccb03
ms.date: 12/05/2018
ms.keywords: LongLongToUInt8, LongLongToUInt8 function [Windows Shell], intsafe/LongLongToUInt8, shell.LongLongToUInt8
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
 - LongLongToUInt8
 - intsafe/LongLongToUInt8
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
 - LongLongToUInt8
---

# LongLongToUInt8 function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>UINT8</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param pu8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

