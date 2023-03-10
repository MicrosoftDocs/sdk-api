---
UID: NF:intsafe.ULongPtrToUInt8
title: ULongPtrToUInt8 function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type UINT8.
helpviewer_keywords: ["ULongPtrToUInt8","ULongPtrToUInt8 function [Windows Shell]","ULongToByte","intsafe/ULongPtrToUInt8","shell.ULongPtrToUInt8"]
old-location: shell\ULongPtrToUInt8.htm
tech.root: shell
ms.assetid: 1a287c22-80d8-4cd9-8878-c19aaeddd407
ms.date: 12/05/2018
ms.keywords: ULongPtrToUInt8, ULongPtrToUInt8 function [Windows Shell], ULongToByte, intsafe/ULongPtrToUInt8, shell.ULongPtrToUInt8
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
 - ULongPtrToUInt8
 - intsafe/ULongPtrToUInt8
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
 - ULongPtrToUInt8
---

# ULongPtrToUInt8 function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>UINT8</b>.

## -parameters

### -param ulOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>ULongToByte</b> is an alias for this function.

