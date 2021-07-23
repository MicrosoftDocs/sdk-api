---
UID: NF:intsafe.ULongLongToUShort
title: ULongLongToUShort function (intsafe.h)
description: Converts a value of type ULONGLONG to a value of type USHORT.
helpviewer_keywords: ["ULongLongToUShort","ULongLongToUShort function [Windows Shell]","intsafe/ULongLongToUShort","shell.ULongLongToUShort"]
old-location: shell\ULongLongToUShort.htm
tech.root: shell
ms.assetid: 7e320c61-31af-485d-a023-dc656798c73a
ms.date: 12/05/2018
ms.keywords: ULongLongToUShort, ULongLongToUShort function [Windows Shell], intsafe/ULongLongToUShort, shell.ULongLongToUShort
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
 - ULongLongToUShort
 - intsafe/ULongLongToUShort
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
 - ULongLongToUShort
---

# ULongLongToUShort function


## -description

Converts a value of type <b>ULONGLONG</b> to a value of type <b>USHORT</b>.

## -parameters

### -param ullOperand [in]

The value to convert.

### -param pusResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

