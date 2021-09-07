---
UID: NF:intsafe.IntToUInt8
title: IntToUInt8 function (intsafe.h)
description: Converts a value of type INT to a value of type UINT8.
helpviewer_keywords: ["IntToByte","IntToUInt8","IntToUInt8 function [Windows Shell]","intsafe/IntToUInt8","shell.IntToUInt8"]
old-location: shell\IntToUInt8.htm
tech.root: shell
ms.assetid: 4c3c8d81-d67b-4e5f-9606-2d21ddaf0786
ms.date: 12/05/2018
ms.keywords: IntToByte, IntToUInt8, IntToUInt8 function [Windows Shell], intsafe/IntToUInt8, shell.IntToUInt8
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
 - IntToUInt8
 - intsafe/IntToUInt8
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
 - IntToUInt8
---

# IntToUInt8 function


## -description

Converts a value of type <b>INT</b> to a value of type <b>UINT8</b>.

## -parameters

### -param iOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IntToByte</b> is an alias for this function.

