---
UID: NF:intsafe.ULongPtrToLongLong
title: ULongPtrToLongLong function
author: windows-driver-content
description: Converts a value of type DWORD_PTR to a value of type INT64.
old-location: shell\DWordPtrToInt64.htm
old-project: shell
ms.assetid: 59060455-0c91-4d9b-a124-069680694b8f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DWordPtrToInt64, DWordPtrToInt64 function [Windows Shell], ULongPtrToLongLong, _shell_DWordPtrToInt64, intsafe/DWordPtrToInt64, shell.DWordPtrToInt64
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
-	DllExport
api_location:
-	None
api_name:
-	DWordPtrToInt64
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongPtrToLongLong function


## -description


Converts a value of type <b>DWORD_PTR</b> to a value of type <b>INT64</b>.


## -parameters




### -param ulOperand

TBD


### -param pllResult

TBD




#### - dwOperand [in]

Type: <b>DWORD_PTR</b>

The value to be converted.


#### - pi64Result [out]

Type: <b>INT64*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



