---
UID: NF:intsafe.ULongToInt8
title: ULongToInt8 function (intsafe.h)
description: Converts a value of type ULONG to a value of type INT8.
helpviewer_keywords: ["ULongToInt8","ULongToInt8 function [Windows Shell]","intsafe/ULongToInt8","shell.ULongToInt8"]
old-location: shell\ULongToInt8.htm
tech.root: shell
ms.assetid: b6c87822-ad6a-4549-925c-f73ef183b27f
ms.date: 12/05/2018
ms.keywords: ULongToInt8, ULongToInt8 function [Windows Shell], intsafe/ULongToInt8, shell.ULongToInt8
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
 - ULongToInt8
 - intsafe/ULongToInt8
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
 - ULongToInt8
---

# ULongToInt8 function


## -description

Converts a value of type <b>ULONG</b> to a value of type <b>INT8</b>.

## -parameters

### -param ulOperand [in]

The value to convert.

### -param pi8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

