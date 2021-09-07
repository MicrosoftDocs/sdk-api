---
UID: NF:intsafe.LongPtrToChar
title: LongPtrToChar function (intsafe.h)
description: Converts a value of type LONG_PTR to a value of type CHAR.
helpviewer_keywords: ["LongPtrToChar","LongPtrToChar function [Windows Shell]","intsafe/LongPtrToChar","shell.LongPtrToChar"]
old-location: shell\LongPtrToChar.htm
tech.root: shell
ms.assetid: 661b7a6f-5524-44e5-9999-61c9df8e7cd3
ms.date: 12/05/2018
ms.keywords: LongPtrToChar, LongPtrToChar function [Windows Shell], intsafe/LongPtrToChar, shell.LongPtrToChar
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
 - LongPtrToChar
 - intsafe/LongPtrToChar
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
 - LongPtrToChar
---

# LongPtrToChar function


## -description

Converts a value of type <b>LONG_PTR</b> to a value of type <b>CHAR</b>.

## -parameters

### -param lOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

