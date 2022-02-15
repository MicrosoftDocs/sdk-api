---
UID: NF:intsafe.ULongPtrToUShort
title: ULongPtrToUShort function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type USHORT.
helpviewer_keywords: ["ULongPtrToUShort","ULongPtrToUShort function [Windows Shell]","intsafe/ULongPtrToUShort","shell.ULongPtrToUShort"]
old-location: shell\ULongPtrToUShort.htm
tech.root: shell
ms.assetid: 0d565dc6-833c-49b4-b01c-13762c946111
ms.date: 12/05/2018
ms.keywords: ULongPtrToUShort, ULongPtrToUShort function [Windows Shell], intsafe/ULongPtrToUShort, shell.ULongPtrToUShort
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
 - ULongPtrToUShort
 - intsafe/ULongPtrToUShort
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
 - ULongPtrToUShort
---

# ULongPtrToUShort function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>USHORT</b>.

## -parameters

### -param ulOperand [in]

The value to convert.

### -param pusResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

