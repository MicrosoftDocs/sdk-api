---
UID: NF:intsafe.LongPtrSub
title: LongPtrSub function (intsafe.h)
description: Subtracts one value of type LONG_PTR from another.
helpviewer_keywords: ["LongPtrSub","LongPtrSub function [Windows Shell]","intsafe/LongPtrSub","shell.LongPtrSub"]
old-location: shell\LongPtrSub.htm
tech.root: shell
ms.assetid: f6e35f6a-9af1-4e14-82c0-0f96ecf01c15
ms.date: 12/05/2018
ms.keywords: LongPtrSub, LongPtrSub function [Windows Shell], intsafe/LongPtrSub, shell.LongPtrSub
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
 - LongPtrSub
 - intsafe/LongPtrSub
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
 - LongPtrSub
---

# LongPtrSub function


## -description

Subtracts one value of type <b>LONG_PTR</b> from another.

## -parameters

### -param lMinuend [in]

The first value.

### -param lSubtrahend [in]

The value to subtract.

### -param plResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

