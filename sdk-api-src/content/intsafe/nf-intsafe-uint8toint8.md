---
UID: NF:intsafe.UInt8ToInt8
title: UInt8ToInt8 function (intsafe.h)
description: Converts a value of type UINT8 to a value of type INT8.
helpviewer_keywords: ["UInt8ToInt8","UInt8ToInt8 function [Windows Shell]","intsafe/UInt8ToInt8","shell.UInt8ToInt8"]
old-location: shell\UInt8ToInt8.htm
tech.root: shell
ms.assetid: e62784c6-0a26-4b3a-a9cc-0ab7b64ff37c
ms.date: 12/05/2018
ms.keywords: UInt8ToInt8, UInt8ToInt8 function [Windows Shell], intsafe/UInt8ToInt8, shell.UInt8ToInt8
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
 - UInt8ToInt8
 - intsafe/UInt8ToInt8
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
 - UInt8ToInt8
---

# UInt8ToInt8 function


## -description

Converts a value of type <b>UINT8</b> to a value of type <b>INT8</b>.

## -parameters

### -param u8Operand [in]

The value to convert.

### -param pi8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

