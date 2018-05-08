---
UID: NF:intsafe.LongPtrToULong
title: LongPtrToULong function
author: windows-driver-content
description: Converts a value of type LONG_PTR to a value of type DWORD.
old-location: shell\LongPtrToDWord.htm
old-project: shell
ms.assetid: 215aa8cc-08a6-466a-827c-4af9500a7ef1
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: LongPtrToDWord, LongPtrToDWord function [Windows Shell], LongPtrToULong, _shell_LongPtrToDWord, intsafe/LongPtrToDWord, shell.LongPtrToDWord
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
-	LongPtrToDWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongPtrToULong function


## -description


Converts a value of type <b>LONG_PTR</b> to a value of type <b>DWORD</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG_PTR</b>

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



