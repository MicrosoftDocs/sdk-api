---
UID: NF:intsafe.ShortToUInt8
title: ShortToUInt8 function (intsafe.h)
description: Converts a value of type SHORT to a value of type UINT8.
helpviewer_keywords: ["ShortToByte","ShortToUInt8","ShortToUInt8 function [Windows Shell]","intsafe/ShortToUInt8","shell.ShortToUInt8"]
old-location: shell\ShortToUInt8.htm
tech.root: shell
ms.assetid: 8e3746c6-fe14-4a98-afcf-0b5981b78677
ms.date: 12/05/2018
ms.keywords: ShortToByte, ShortToUInt8, ShortToUInt8 function [Windows Shell], intsafe/ShortToUInt8, shell.ShortToUInt8
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
 - ShortToUInt8
 - intsafe/ShortToUInt8
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
 - ShortToUInt8
---

# ShortToUInt8 function


## -description

Converts a value of type <b>SHORT</b> to a value of type <b>UINT8</b>.

## -parameters

### -param sOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>ShortToByte</b> is an alias for this function.

