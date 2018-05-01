---
UID: NF:intsafe.LongToULong
title: LongToULong function
author: windows-driver-content
description: Converts a value of type LONG to a value of type DWORD.
old-location: shell\LongToDWord.htm
old-project: shell
ms.assetid: 164306d8-dfc1-4aee-baa8-2a0f57253c70
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: LongToDWord, LongToDWord function [Windows Shell], LongToULong, _shell_LongToDWord, intsafe/LongToDWord, shell.LongToDWord
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
-	LongToDWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongToULong function


## -description


Converts a value of type <b>LONG</b> to a value of type <b>DWORD</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG</b>

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



