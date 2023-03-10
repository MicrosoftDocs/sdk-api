---
UID: NF:intsafe.UIntPtrToUInt8
title: UIntPtrToUInt8 function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type UINT8.
helpviewer_keywords: ["UIntPtrToUInt8","UIntPtrToUInt8 function [Windows Shell]","intsafe/UIntPtrToUInt8","shell.UIntPtrToUInt8"]
old-location: shell\UIntPtrToUInt8.htm
tech.root: shell
ms.assetid: 5490bca2-52c8-4e98-a2ac-137aa7c423de
ms.date: 12/05/2018
ms.keywords: UIntPtrToUInt8, UIntPtrToUInt8 function [Windows Shell], intsafe/UIntPtrToUInt8, shell.UIntPtrToUInt8
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
 - UIntPtrToUInt8
 - intsafe/UIntPtrToUInt8
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
 - UIntPtrToUInt8
---

# UIntPtrToUInt8 function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>UINT8</b>.

## -parameters

### -param uOperand [in]

The value to convert.

### -param pu8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

