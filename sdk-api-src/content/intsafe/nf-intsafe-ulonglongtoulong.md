---
UID: NF:intsafe.ULongLongToULong
title: ULongLongToULong function
author: windows-driver-content
description: Converts a value of type ULONGLONG to a value of type DWORD.
old-location: shell\ULongLongToDWord.htm
old-project: shell
ms.assetid: 7b3c3d2d-e509-4b55-88aa-1d183ab0a41c
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ULongLongToDWord, ULongLongToDWord function [Windows Shell], ULongLongToULong, _shell_ULongLongToDWord, intsafe/ULongLongToDWord, shell.ULongLongToDWord
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
-	ULongLongToDWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongToULong function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>DWORD</b>.


## -parameters




### -param ullOperand [in]

Type: <b>ULONGLONG</b>

The value to be converted.


### -param pulResult

TBD




#### - pdwResult [out]

Type: <b>DWORD*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



