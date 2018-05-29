---
UID: NF:intsafe.UIntPtrToInt
title: UIntPtrToInt function
author: windows-sdk-content
description: Converts a value of type SIZE_T to a value of type INT.
old-location: shell\SIZETToInt_1.htm
old-project: shell
ms.assetid: 00a1229b-28cf-4d8e-a59a-0c91872b2e06
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SIZETToInt, SIZETToInt function [Windows Shell], UIntPtrToInt, _shell_SIZETToInt, intsafe/SIZETToInt, shell.SIZETToInt, shell.SIZETToInt_1
ms.prod: windows
ms.technology: windows-sdk
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
-	SIZETToInt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToInt function


## -description


Converts a value of type <b>SIZE_T</b> to a value of type <b>INT</b>.


## -parameters




### -param uOperand

TBD


### -param piResult [out]

Type: <b>INT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - cbOperand [in]

Type: <b>SIZE_T</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



