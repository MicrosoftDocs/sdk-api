---
UID: NF:intsafe.IntPtrToUChar
title: IntPtrToUChar function (intsafe.h)
description: Converts a value of type INT_PTR to a value of type UCHAR.
old-location: shell\IntPtrToUChar.htm
tech.root: shell
ms.assetid: f6428be2-bca6-4fda-a247-0f0eff2483d8
ms.date: 12/05/2018
ms.keywords: IntPtrToUChar, IntPtrToUChar function [Windows Shell], intsafe/IntPtrToUChar, shell.IntPtrToUChar
ms.topic: function
f1_keywords:
- intsafe/IntPtrToUChar
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- intsafe.h
api_name:
- IntPtrToUChar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IntPtrToUChar function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>UCHAR</b>.


## -parameters




### -param iOperand [in]

The value to convert.


### -param pch [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



