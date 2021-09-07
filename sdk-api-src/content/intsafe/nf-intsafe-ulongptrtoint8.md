---
UID: NF:intsafe.ULongPtrToInt8
title: ULongPtrToInt8 function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type INT8.
helpviewer_keywords: ["ULongPtrToInt8","ULongPtrToInt8 function [Windows Shell]","intsafe/ULongPtrToInt8","shell.ULongPtrToInt8"]
old-location: shell\ULongPtrToInt8.htm
tech.root: shell
ms.assetid: 097e43ef-0d7a-4533-9dc6-68f41df2e734
ms.date: 12/05/2018
ms.keywords: ULongPtrToInt8, ULongPtrToInt8 function [Windows Shell], intsafe/ULongPtrToInt8, shell.ULongPtrToInt8
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
 - ULongPtrToInt8
 - intsafe/ULongPtrToInt8
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
 - ULongPtrToInt8
---

# ULongPtrToInt8 function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>INT8</b>.

## -parameters

### -param ulOperand [in]

The value to convert.

### -param pi8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

