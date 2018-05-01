---
UID: NF:intsafe.ULongLongToLongLong
title: ULongLongToLongLong function
author: windows-driver-content
description: Converts a value of type ULONGLONG to a value of type INT64.
old-location: shell\ULongLongToInt64.htm
old-project: shell
ms.assetid: 6dff4953-1469-491f-a31b-5e7fe72d0fb7
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ULongLongToInt64, ULongLongToInt64 function [Windows Shell], ULongLongToLongLong, _shell_ULongLongToInt64, intsafe/ULongLongToInt64, shell.ULongLongToInt64
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
-	ULongLongToInt64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongToLongLong function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>INT64</b>.


## -parameters




### -param ullOperand [in]

Type: <b>ULONGLONG</b>

The value to be converted.


### -param pllResult

TBD




#### - pi64Result [out]

Type: <b>INT64*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



