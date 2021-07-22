---
UID: NF:intsafe.ULongPtrToUChar
title: ULongPtrToUChar function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type UCHAR.
helpviewer_keywords: ["ULongPtrToUChar","ULongPtrToUChar function [Windows Shell]","intsafe/ULongPtrToUChar","shell.ULongPtrToUChar"]
old-location: shell\ULongPtrToUChar.htm
tech.root: shell
ms.assetid: ed18b6c7-0ee3-41b4-a73c-83926fd62798
ms.date: 12/05/2018
ms.keywords: ULongPtrToUChar, ULongPtrToUChar function [Windows Shell], intsafe/ULongPtrToUChar, shell.ULongPtrToUChar
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
 - ULongPtrToUChar
 - intsafe/ULongPtrToUChar
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
 - ULongPtrToUChar
---

# ULongPtrToUChar function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>UCHAR</b>.

## -parameters

### -param ulOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

