---
UID: NF:intsafe.Int8ToUIntPtr
title: Int8ToUIntPtr function (intsafe.h)
description: Converts a value of type INT8 to a value of type UINT_PTR.
helpviewer_keywords: ["Int8ToUIntPtr","Int8ToUIntPtr function [Windows Shell]","intsafe/Int8ToUIntPtr","shell.Int8ToUIntPtr"]
old-location: shell\Int8ToUIntPtr.htm
tech.root: shell
ms.assetid: 9b40adbe-c1df-4abd-b76e-839c04562d3d
ms.date: 12/05/2018
ms.keywords: Int8ToUIntPtr, Int8ToUIntPtr function [Windows Shell], intsafe/Int8ToUIntPtr, shell.Int8ToUIntPtr
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
 - Int8ToUIntPtr
 - intsafe/Int8ToUIntPtr
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
 - Int8ToUIntPtr
---

# Int8ToUIntPtr function


## -description

Converts a value of type <b>INT8</b> to a value of type <b>UINT_PTR</b>.

## -parameters

### -param i8Operand [in]

The value to convert.

### -param puResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

