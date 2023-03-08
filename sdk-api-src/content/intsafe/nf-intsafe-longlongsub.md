---
UID: NF:intsafe.LongLongSub
title: LongLongSub function (intsafe.h)
description: Subtracts one value of type LONGLONG from another.
helpviewer_keywords: ["LongLongSub","LongLongSub function [Windows Shell]","intsafe/LongLongSub","shell.LongLongSub"]
old-location: shell\LongLongSub.htm
tech.root: shell
ms.assetid: 8c6c65c7-0f93-4823-a6f3-cc59c4b5b207
ms.date: 12/05/2018
ms.keywords: LongLongSub, LongLongSub function [Windows Shell], intsafe/LongLongSub, shell.LongLongSub
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
 - LongLongSub
 - intsafe/LongLongSub
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
 - LongLongSub
---

# LongLongSub function


## -description

Subtracts one value of type <b>LONGLONG</b> from another.

## -parameters

### -param llMinuend [in]

The first value.

### -param llSubtrahend [in]

The value to subtract.

### -param pllResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

