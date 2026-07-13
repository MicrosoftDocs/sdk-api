---
UID: NF:intsafe.LongPtrAdd
title: LongPtrAdd function (intsafe.h)
description: Adds two values of type LONG_PTR.
helpviewer_keywords: ["LongPtrAdd","LongPtrAdd function [Windows Shell]","intsafe/LongPtrAdd","shell.LongPtrAdd"]
old-location: shell\LongPtrAdd.htm
tech.root: shell
ms.assetid: 1c5f3112-12f1-409f-9a0f-74d4d35abb48
ms.date: 12/05/2018
ms.keywords: LongPtrAdd, LongPtrAdd function [Windows Shell], intsafe/LongPtrAdd, shell.LongPtrAdd
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
 - LongPtrAdd
 - intsafe/LongPtrAdd
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
 - LongPtrAdd
---

# LongPtrAdd function


## -description

Adds two values of type <b>LONG_PTR</b>.

## -parameters

### -param lAugend [in]

The first value.

### -param lAddend [in]

The second value.

### -param plResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

