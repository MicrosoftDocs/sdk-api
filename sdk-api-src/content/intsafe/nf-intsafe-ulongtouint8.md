---
UID: NF:intsafe.ULongToUInt8
title: ULongToUInt8 function (intsafe.h)
description: Converts a value of type ULONG to a value of type UINT8.
helpviewer_keywords: ["DWordToByte","ULongToUInt8","ULongToUInt8 function [Windows Shell]","intsafe/ULongToUInt8","shell.ULongToUInt8"]
old-location: shell\ULongToUInt8.htm
tech.root: shell
ms.assetid: 2d1db351-797f-4785-b67c-9ab6e661282a
ms.date: 12/05/2018
ms.keywords: DWordToByte, ULongToUInt8, ULongToUInt8 function [Windows Shell], intsafe/ULongToUInt8, shell.ULongToUInt8
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
 - ULongToUInt8
 - intsafe/ULongToUInt8
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
 - ULongToUInt8
---

# ULongToUInt8 function


## -description

Converts a value of type <b>ULONG</b> to a value of type <b>UINT8</b>.

## -parameters

### -param ulOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>DWordToByte</b> is an alias for this function.

