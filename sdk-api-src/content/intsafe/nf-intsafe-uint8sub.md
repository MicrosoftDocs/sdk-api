---
UID: NF:intsafe.UInt8Sub
title: UInt8Sub function (intsafe.h)
description: Subtracts one value of type UINT8 from another.
helpviewer_keywords: ["UInt8Sub","UInt8Sub function [Windows Shell]","intsafe/UInt8Sub","shell.UInt8Sub"]
old-location: shell\UInt8Sub.htm
tech.root: shell
ms.assetid: 3c140c21-7185-4342-bc40-d6382944e423
ms.date: 12/05/2018
ms.keywords: UInt8Sub, UInt8Sub function [Windows Shell], intsafe/UInt8Sub, shell.UInt8Sub
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
 - UInt8Sub
 - intsafe/UInt8Sub
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
 - UInt8Sub
---

# UInt8Sub function


## -description

Subtracts one value of type <b>UINT8</b> from another.

## -parameters

### -param u8Minuend [in]

The first value.

### -param u8Subtrahend [in]

The value to subtract.

### -param pu8Result [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

