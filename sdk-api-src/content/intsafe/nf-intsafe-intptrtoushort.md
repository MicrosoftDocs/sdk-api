---
UID: NF:intsafe.IntPtrToUShort
title: IntPtrToUShort function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type USHORT.
helpviewer_keywords: ["IntPtrToUShort","IntPtrToUShort function [Windows Shell]","intsafe/IntPtrToUShort","shell.IntPtrToUShort"]
old-location: shell\IntPtrToUShort.htm
tech.root: shell
ms.assetid: c1ab8cbc-0c45-410c-a34d-2bded36a03e8
ms.date: 12/05/2018
ms.keywords: IntPtrToUShort, IntPtrToUShort function [Windows Shell], intsafe/IntPtrToUShort, shell.IntPtrToUShort
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
 - IntPtrToUShort
 - intsafe/IntPtrToUShort
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
 - IntPtrToUShort
---

# IntPtrToUShort function


## -description

Converts a value of type <b>INT_PTR</b> to a value of type <b>USHORT</b>.

## -parameters

### -param iOperand [in]

The value to convert.

### -param pusResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

