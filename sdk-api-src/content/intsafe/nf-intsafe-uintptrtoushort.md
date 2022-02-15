---
UID: NF:intsafe.UIntPtrToUShort
title: UIntPtrToUShort function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type USHORT.
helpviewer_keywords: ["UIntPtrToUShort","UIntPtrToUShort function [Windows Shell]","intsafe/UIntPtrToUShort","shell.UIntPtrToUShort"]
old-location: shell\UIntPtrToUShort.htm
tech.root: shell
ms.assetid: b51c9d90-861b-40c7-b81d-2c308fc98fd1
ms.date: 12/05/2018
ms.keywords: UIntPtrToUShort, UIntPtrToUShort function [Windows Shell], intsafe/UIntPtrToUShort, shell.UIntPtrToUShort
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
 - UIntPtrToUShort
 - intsafe/UIntPtrToUShort
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
 - UIntPtrToUShort
---

# UIntPtrToUShort function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>USHORT</b>.

## -parameters

### -param uOperand [in]

The value to convert.

### -param pusResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

