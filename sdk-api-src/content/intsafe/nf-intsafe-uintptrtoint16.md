---
UID: NF:intsafe.UIntPtrToInt16
title: UIntPtrToInt16 function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type INT16.
helpviewer_keywords: ["UIntPtrToInt16","UIntPtrToInt16 function [Windows Shell]","intsafe/UIntPtrToInt16","shell.UIntPtrToInt16"]
old-location: shell\UIntPtrToInt16.htm
tech.root: shell
ms.assetid: cce027f0-34e9-4c13-89de-102c98ab7a14
ms.date: 12/05/2018
ms.keywords: UIntPtrToInt16, UIntPtrToInt16 function [Windows Shell], intsafe/UIntPtrToInt16, shell.UIntPtrToInt16
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
 - UIntPtrToInt16
 - intsafe/UIntPtrToInt16
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
 - UIntPtrToInt16
---

# UIntPtrToInt16 function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>INT16</b>.

## -parameters

### -param uOperand [in]

The value to convert.

### -param pi16Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

