---
UID: NF:intsafe.UIntPtrToChar
title: UIntPtrToChar function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type CHAR.
helpviewer_keywords: ["UIntPtrToChar","UIntPtrToChar function [Windows Shell]","intsafe/UIntPtrToChar","shell.UIntPtrToChar"]
old-location: shell\UIntPtrToChar.htm
tech.root: shell
ms.assetid: b98ec1ee-8439-494b-b8e6-aa3d127042fa
ms.date: 12/05/2018
ms.keywords: UIntPtrToChar, UIntPtrToChar function [Windows Shell], intsafe/UIntPtrToChar, shell.UIntPtrToChar
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
 - UIntPtrToChar
 - intsafe/UIntPtrToChar
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
 - UIntPtrToChar
---

# UIntPtrToChar function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>CHAR</b>.

## -parameters

### -param uOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

