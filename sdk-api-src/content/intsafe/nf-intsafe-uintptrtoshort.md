---
UID: NF:intsafe.UIntPtrToShort
title: UIntPtrToShort function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type SHORT.
helpviewer_keywords: ["UIntPtrToShort","UIntPtrToShort function [Windows Shell]","intsafe/UIntPtrToShort","shell.UIntPtrToShort"]
old-location: shell\UIntPtrToShort.htm
tech.root: shell
ms.assetid: 6cbbced2-5a0f-49d6-8ac0-27a9d1a885fe
ms.date: 12/05/2018
ms.keywords: UIntPtrToShort, UIntPtrToShort function [Windows Shell], intsafe/UIntPtrToShort, shell.UIntPtrToShort
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
 - UIntPtrToShort
 - intsafe/UIntPtrToShort
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
 - UIntPtrToShort
---

# UIntPtrToShort function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>SHORT</b>.

## -parameters

### -param uOperand [in]

The value to convert.

### -param psResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

