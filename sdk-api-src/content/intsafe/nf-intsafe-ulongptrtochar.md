---
UID: NF:intsafe.ULongPtrToChar
title: ULongPtrToChar function (intsafe.h)
description: Converts a value of type ULONG_PTR to a value of type CHAR.
helpviewer_keywords: ["ULongPtrToChar","ULongPtrToChar function [Windows Shell]","intsafe/ULongPtrToChar","shell.ULongPtrToChar"]
old-location: shell\ULongPtrToChar.htm
tech.root: shell
ms.assetid: 0cc26423-5c14-49d0-984e-f2bb81f68010
ms.date: 12/05/2018
ms.keywords: ULongPtrToChar, ULongPtrToChar function [Windows Shell], intsafe/ULongPtrToChar, shell.ULongPtrToChar
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
 - ULongPtrToChar
 - intsafe/ULongPtrToChar
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
 - ULongPtrToChar
---

# ULongPtrToChar function


## -description

Converts a value of type <b>ULONG_PTR</b> to a value of type <b>CHAR</b>.

## -parameters

### -param ulOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

