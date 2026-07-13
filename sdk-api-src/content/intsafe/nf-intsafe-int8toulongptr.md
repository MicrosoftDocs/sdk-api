---
UID: NF:intsafe.Int8ToULongPtr
title: Int8ToULongPtr function (intsafe.h)
description: Converts a value of type INT8 to a value of type ULONG_PTR.
helpviewer_keywords: ["Int8ToULongPtr","Int8ToULongPtr function [Windows Shell]","intsafe/Int8ToULongPtr","shell.Int8ToULongPtr"]
old-location: shell\Int8ToULongPtr.htm
tech.root: shell
ms.assetid: 84a9003a-1f80-4dea-8062-888097963e47
ms.date: 12/05/2018
ms.keywords: Int8ToULongPtr, Int8ToULongPtr function [Windows Shell], intsafe/Int8ToULongPtr, shell.Int8ToULongPtr
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
 - Int8ToULongPtr
 - intsafe/Int8ToULongPtr
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
 - Int8ToULongPtr
---

# Int8ToULongPtr function


## -description

Converts a value of type <b>INT8</b> to a value of type <b>ULONG_PTR</b>.

## -parameters

### -param i8Operand [in]

The value to convert.

### -param pulResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

