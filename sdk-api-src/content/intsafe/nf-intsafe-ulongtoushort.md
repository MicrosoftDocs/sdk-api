---
UID: NF:intsafe.ULongToUShort
title: ULongToUShort function
author: windows-driver-content
description: Converts a value of type DWORD to a value of type WORD.
old-location: shell\DWordToWord.htm
old-project: shell
ms.assetid: 677ecdbc-197e-461e-aeab-5c73662fbf16
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: DWordToWord, DWordToWord function [Windows Shell], ULongToUShort, _shell_DWordToWord, intsafe/DWordToWord, shell.DWordToWord
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
-	DWordToWord
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongToUShort function


## -description


Converts a value of type <b>DWORD</b> to a value of type <b>WORD</b>.


## -parameters




### -param ulOperand

TBD


### -param pusResult

TBD




#### - dwOperand [in]

Type: <b>DWORD</b>

The value to be converted.


#### - pwResult [out]

Type: <b>WORD*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



