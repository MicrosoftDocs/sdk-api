---
UID: NF:intsafe.UIntPtrToLongLong
title: UIntPtrToLongLong function
author: windows-driver-content
description: Converts a value of type size_t to a value of type INT64.
old-location: shell\SizeTToInt64.htm
old-project: shell
ms.assetid: be089335-f709-4425-b9d5-3663dcca9e41
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: SizeTToInt64, SizeTToInt64 function [Windows Shell], UIntPtrToLongLong, _shell_SizeTToInt64, intsafe/SizeTToInt64, shell.SizeTToInt64
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
-	SizeTToInt64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToLongLong function


## -description


Converts a value of type <b>size_t</b> to a value of type <b>INT64</b>.


## -parameters




### -param uOperand

TBD


### -param pllResult

TBD




#### - cbOperand [in]

Type: <b>size_t</b>

The value to be converted.


#### - pi64Result [out]

Type: <b>INT64*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



