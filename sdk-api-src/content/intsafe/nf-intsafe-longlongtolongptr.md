---
UID: NF:intsafe.LongLongToLongPtr
title: LongLongToLongPtr function
author: windows-driver-content
description: Converts a value of type INT64 to a value of type LONG_PTR.
old-location: shell\Int64ToLongPtr.htm
old-project: shell
ms.assetid: 583c9a4a-698e-4df7-a4aa-9f76de5e8a65
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Int64ToLongPtr, Int64ToLongPtr function [Windows Shell], LongLongToLongPtr, _shell_Int64ToLongPtr, intsafe/Int64ToLongPtr, shell.Int64ToLongPtr
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
-	Int64ToLongPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToLongPtr function


## -description


Converts a value of type <b>INT64</b> to a value of type <b>LONG_PTR</b>.


## -parameters




### -param llOperand

TBD


### -param plResult [out]

Type: <b>LONG_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - i64Operand [in]

Type: <b>INT64</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



