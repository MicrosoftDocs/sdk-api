---
UID: NF:intsafe.PtrdiffTSub
title: PtrdiffTSub function (intsafe.h)
description: Subtracts one value of type ptrdiff_t from another.
helpviewer_keywords: ["PtrdiffTSub","PtrdiffTSub function [Windows Shell]","intsafe/PtrdiffTSub","shell.PtrdiffTSub"]
old-location: shell\PtrdiffTSub.htm
tech.root: shell
ms.assetid: 633ba8f5-ce8b-41a0-8af3-c06f69c9b676
ms.date: 12/05/2018
ms.keywords: PtrdiffTSub, PtrdiffTSub function [Windows Shell], intsafe/PtrdiffTSub, shell.PtrdiffTSub
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
 - PtrdiffTSub
 - intsafe/PtrdiffTSub
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
 - PtrdiffTSub
---

# PtrdiffTSub function


## -description

Subtracts one value of type <b>ptrdiff_t</b> from another.

## -parameters

### -param Minuend [in]

The first value.

### -param Subtrahend [in]

The value to subtract.

### -param pResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

