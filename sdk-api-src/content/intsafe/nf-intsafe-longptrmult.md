---
UID: NF:intsafe.LongPtrMult
title: LongPtrMult function (intsafe.h)
description: Multiplies two values of type LONG_PTR.
helpviewer_keywords: ["LongPtrMult","LongPtrMult function [Windows Shell]","intsafe/LongPtrMult","shell.LongPtrMult"]
old-location: shell\LongPtrMult.htm
tech.root: shell
ms.assetid: c2b86515-fe03-439a-bfe4-d92750b29279
ms.date: 12/05/2018
ms.keywords: LongPtrMult, LongPtrMult function [Windows Shell], intsafe/LongPtrMult, shell.LongPtrMult
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
 - LongPtrMult
 - intsafe/LongPtrMult
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
 - LongPtrMult
---

# LongPtrMult function


## -description

Multiplies two values of type <b>LONG_PTR</b>.

## -parameters

### -param lMultiplicand [in]

The first value.

### -param lMultiplier [in]

The second value.

### -param plResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

