---
UID: NF:intsafe.IntSub
title: IntSub function (intsafe.h)
description: Subtracts one value of type INT from another.
helpviewer_keywords: ["IntSub","IntSub function [Windows Shell]","intsafe/IntSub","shell.IntSub"]
old-location: shell\IntSub.htm
tech.root: shell
ms.assetid: ee083a68-27fd-4c94-93e0-7e662c48d5cf
ms.date: 12/05/2018
ms.keywords: IntSub, IntSub function [Windows Shell], intsafe/IntSub, shell.IntSub
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
 - IntSub
 - intsafe/IntSub
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
 - IntSub
---

# IntSub function


## -description

Subtracts one value of type <b>INT</b> from another.

## -parameters

### -param iMinuend [in]

The first value.

### -param iSubtrahend [in]

The value to subtract.

### -param piResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

