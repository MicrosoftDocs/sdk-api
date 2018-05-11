---
UID: NF:intsafe.LongLongToULongLong
title: LongLongToULongLong function
author: windows-driver-content
description: Converts a value of type INT64 to a value of type ULONGLONG.
old-location: shell\Int64ToULongLong.htm
old-project: shell
ms.assetid: c1cc723c-6f03-4517-849c-eac31393dc53
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Int64ToULongLong, Int64ToULongLong function [Windows Shell], LongLongToULongLong, _shell_Int64ToULongLong, intsafe/Int64ToULongLong, shell.Int64ToULongLong
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
-	Int64ToULongLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToULongLong function


## -description


Converts a value of type <b>INT64</b> to a value of type <b>ULONGLONG</b>.


## -parameters




### -param llOperand

TBD


### -param pullResult [out]

Type: <b>ULONGLONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - i64Operand [in]

Type: <b>INT64</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



