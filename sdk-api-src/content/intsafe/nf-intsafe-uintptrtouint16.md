---
UID: NF:intsafe.UIntPtrToUInt16
title: UIntPtrToUInt16 function (intsafe.h)
description: Converts a value of type UINT_PTR to a value of type UINT16.
helpviewer_keywords: ["UIntPtrToUInt16","UIntPtrToUInt16 function [Windows Shell]","intsafe/UIntPtrToUInt16","shell.UIntPtrToUInt16"]
old-location: shell\UIntPtrToUInt16.htm
tech.root: shell
ms.assetid: ff01f865-5955-48a6-abcd-205488028f00
ms.date: 12/05/2018
ms.keywords: UIntPtrToUInt16, UIntPtrToUInt16 function [Windows Shell], intsafe/UIntPtrToUInt16, shell.UIntPtrToUInt16
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
 - UIntPtrToUInt16
 - intsafe/UIntPtrToUInt16
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
 - UIntPtrToUInt16
---

# UIntPtrToUInt16 function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>UINT16</b>.

## -parameters

### -param uOperand [in]

The value to convert.

### -param pu16Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

