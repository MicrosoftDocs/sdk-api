---
UID: NF:intsafe.IntPtrToUInt8
title: IntPtrToUInt8 function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type UINT8.
helpviewer_keywords: ["IntPtrToUInt8","IntPtrToUInt8 function [Windows Shell]","intsafe/IntPtrToUInt8","shell.IntPtrToUInt8"]
old-location: shell\IntPtrToUInt8.htm
tech.root: shell
ms.assetid: d1337a8a-0a7a-41a1-b57b-f20d8a616113
ms.date: 12/05/2018
ms.keywords: IntPtrToUInt8, IntPtrToUInt8 function [Windows Shell], intsafe/IntPtrToUInt8, shell.IntPtrToUInt8
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
 - IntPtrToUInt8
 - intsafe/IntPtrToUInt8
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
 - IntPtrToUInt8
---

# IntPtrToUInt8 function


## -description

Converts a value of type <b>INT_PTR</b> to a value of type <b>UINT8</b>.

## -parameters

### -param iOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

