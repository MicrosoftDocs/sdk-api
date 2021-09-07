---
UID: NF:intsafe.UIntToUInt8
title: UIntToUInt8 function (intsafe.h)
description: Converts a value of type UINT to a value of type UINT8.
helpviewer_keywords: ["UIntToByte","UIntToUInt8","UIntToUInt8 function [Windows Shell]","intsafe/UIntToUInt8","shell.UIntToUInt8"]
old-location: shell\UIntToUInt8.htm
tech.root: shell
ms.assetid: c3c63264-6b5d-4d58-947a-d0cc7a051a6d
ms.date: 12/05/2018
ms.keywords: UIntToByte, UIntToUInt8, UIntToUInt8 function [Windows Shell], intsafe/UIntToUInt8, shell.UIntToUInt8
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
 - UIntToUInt8
 - intsafe/UIntToUInt8
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
 - UIntToUInt8
---

# UIntToUInt8 function


## -description

Converts a value of type <b>UINT</b> to a value of type <b>UINT8</b>.

## -parameters

### -param uOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>UIntToByte</b> is an alias for this function.

