---
UID: NF:intsafe.Int8ToUInt8
title: Int8ToUInt8 function (intsafe.h)
description: Converts a value of type INT8 to a value of type UINT8.
helpviewer_keywords: ["Int8ToUInt8","Int8ToUInt8 function [Windows Shell]","intsafe/Int8ToUInt8","shell.Int8ToUInt8"]
old-location: shell\Int8ToUInt8.htm
tech.root: shell
ms.assetid: 1638bfca-9cec-4d01-b3b0-47a4358e35d1
ms.date: 12/05/2018
ms.keywords: Int8ToUInt8, Int8ToUInt8 function [Windows Shell], intsafe/Int8ToUInt8, shell.Int8ToUInt8
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
 - Int8ToUInt8
 - intsafe/Int8ToUInt8
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
 - Int8ToUInt8
---

# Int8ToUInt8 function


## -description

Converts a value of type <b>INT8</b> to a value of type <b>UINT8</b>.

## -parameters

### -param i8Operand [in]

The value to convert.

### -param pu8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

