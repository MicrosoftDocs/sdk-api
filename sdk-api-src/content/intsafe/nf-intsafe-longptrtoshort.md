---
UID: NF:intsafe.LongPtrToShort
title: LongPtrToShort function (intsafe.h)
description: Converts a value of type LONG_PTR to a value of type SHORT.
helpviewer_keywords: ["LongPtrToShort","LongPtrToShort function [Windows Shell]","intsafe/LongPtrToShort","shell.LongPtrToShort"]
old-location: shell\LongPtrToShort.htm
tech.root: shell
ms.assetid: db3236c4-0eac-4484-b36c-fcfa3e148b42
ms.date: 12/05/2018
ms.keywords: LongPtrToShort, LongPtrToShort function [Windows Shell], intsafe/LongPtrToShort, shell.LongPtrToShort
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
 - LongPtrToShort
 - intsafe/LongPtrToShort
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
 - LongPtrToShort
---

# LongPtrToShort function


## -description

Converts a value of type <b>LONG_PTR</b> to a value of type <b>SHORT</b>.

## -parameters

### -param lOperand [in]

The value to convert.

### -param psResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

