---
UID: NF:intsafe.LongLongToShort
title: LongLongToShort function (intsafe.h)
description: Converts a value of type LONGLONG to a value of type SHORT.
helpviewer_keywords: ["LongLongToShort","LongLongToShort function [Windows Shell]","intsafe/LongLongToShort","shell.LongLongToShort"]
old-location: shell\LongLongToShort.htm
tech.root: shell
ms.assetid: c292f2f0-18c3-4675-8ff9-8c773aa6dc8e
ms.date: 12/05/2018
ms.keywords: LongLongToShort, LongLongToShort function [Windows Shell], intsafe/LongLongToShort, shell.LongLongToShort
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
 - LongLongToShort
 - intsafe/LongLongToShort
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
 - LongLongToShort
---

# LongLongToShort function


## -description

Converts a value of type <b>LONGLONG</b> to a value of type <b>SHORT</b>.

## -parameters

### -param llOperand [in]

The value to convert.

### -param psResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

