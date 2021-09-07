---
UID: NF:intsafe.ShortToUIntPtr
title: ShortToUIntPtr function (intsafe.h)
description: Converts a value of type SHORT to a value of type UINT_PTR.
helpviewer_keywords: ["ShortToUIntPtr","ShortToUIntPtr function [Windows Shell]","intsafe/ShortToUIntPtr","shell.ShortToUIntPtr"]
old-location: shell\ShortToUIntPtr.htm
tech.root: shell
ms.assetid: 6b5d0c0c-a2c3-4d63-ab6c-d93372a7413e
ms.date: 12/05/2018
ms.keywords: ShortToUIntPtr, ShortToUIntPtr function [Windows Shell], intsafe/ShortToUIntPtr, shell.ShortToUIntPtr
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
 - ShortToUIntPtr
 - intsafe/ShortToUIntPtr
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
 - ShortToUIntPtr
---

# ShortToUIntPtr function


## -description

Converts a value of type <b>SHORT</b> to a value of type <b>UINT_PTR</b>.

## -parameters

### -param sOperand [in]

The value to convert.

### -param puResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

