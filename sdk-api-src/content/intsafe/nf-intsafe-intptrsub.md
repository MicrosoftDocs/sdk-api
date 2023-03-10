---
UID: NF:intsafe.IntPtrSub
title: IntPtrSub function (intsafe.h)
description: Subtracts one value of type INT_PTR from another.
helpviewer_keywords: ["IntPtrSub","IntPtrSub function [Windows Shell]","intsafe/IntPtrSub","shell.IntPtrSub"]
old-location: shell\IntPtrSub.htm
tech.root: shell
ms.assetid: ad30f236-7412-401f-b6a9-76b74118092d
ms.date: 12/05/2018
ms.keywords: IntPtrSub, IntPtrSub function [Windows Shell], intsafe/IntPtrSub, shell.IntPtrSub
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
 - IntPtrSub
 - intsafe/IntPtrSub
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
 - IntPtrSub
---

# IntPtrSub function


## -description

Subtracts one value of type <b>INT_PTR</b> from another.

## -parameters

### -param iMinuend [in]

The first value.

### -param iSubtrahend [in]

The value to subtract.

### -param piResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

