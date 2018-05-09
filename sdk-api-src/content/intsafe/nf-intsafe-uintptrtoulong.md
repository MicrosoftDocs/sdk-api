---
UID: NF:intsafe.UIntPtrToULong
title: UIntPtrToULong function
author: windows-driver-content
description: Converts a value of type SIZE_T to a value of type DWORD.
old-location: shell\SIZETToDWord_1.htm
old-project: shell
ms.assetid: f56eb5fc-e4d4-4e42-bc4d-375046761f4d
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: SIZETToDWord, SIZETToDWord function [Windows Shell], UIntPtrToULong, _shell_SIZETToDWord, intsafe/SIZETToDWord, shell.SIZETToDWord, shell.SIZETToDWord_1
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
-	SIZETToDWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToULong function


## -description


Converts a value of type <b>SIZE_T</b> to a value of type <b>DWORD</b>.


## -parameters




### -param uOperand

TBD


### -param pulResult

TBD




#### - cbOperand [in]

Type: <b>SIZE_T</b>

The value to be converted.


#### - pdwResult [out]

Type: <b>DWORD*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



