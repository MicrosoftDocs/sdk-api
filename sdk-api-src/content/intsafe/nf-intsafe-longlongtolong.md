---
UID: NF:intsafe.LongLongToLong
title: LongLongToLong function
author: windows-driver-content
description: Converts a value of type INT64 to a value of type LONG.
old-location: shell\Int64ToLong.htm
old-project: shell
ms.assetid: 699d8062-9bd5-4cb2-83fa-0cd120f50ce3
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: Int64ToLong, Int64ToLong function [Windows Shell], LongLongToLong, _shell_Int64ToLong, intsafe/Int64ToLong, shell.Int64ToLong
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Intsafe.h
api_name:
-	Int64ToLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToLong function


## -description


Converts a value of type <b>INT64</b> to a value of type <b>LONG</b>.


## -parameters




### -param llOperand

TBD


### -param plResult [out]

Type: <b>LONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - i64Operand [in]

Type: <b>INT64</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



