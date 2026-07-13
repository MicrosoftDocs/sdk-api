---
UID: NF:intsafe.LongSub
title: LongSub function (intsafe.h)
description: Subtracts one value of type LONG from another.
helpviewer_keywords: ["LongSub","LongSub function [Windows Shell]","intsafe/LongSub","shell.LongSub"]
old-location: shell\LongSub.htm
tech.root: shell
ms.assetid: 8691044c-0706-4fff-a8fe-3ac9ad22de64
ms.date: 12/05/2018
ms.keywords: LongSub, LongSub function [Windows Shell], intsafe/LongSub, shell.LongSub
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
 - LongSub
 - intsafe/LongSub
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
 - LongSub
---

# LongSub function


## -description

Subtracts one value of type <b>LONG</b> from another.

## -parameters

### -param lMinuend [in]

The first value.

### -param lSubtrahend [in]

The value to subtract.

### -param plResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

