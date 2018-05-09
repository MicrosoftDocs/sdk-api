---
UID: NF:intsafe.ULongToChar
title: ULongToChar function
author: windows-driver-content
description: Converts a value of type DWORD to a value of type CHAR.
old-location: shell\DWordToChar.htm
old-project: shell
ms.assetid: 2d3d4114-53ec-420b-93e3-cddb7ae14413
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DWordToChar, DWordToChar function [Windows Shell], ULongToChar, _shell_DWordToChar, intsafe/DWordToChar, shell.DWordToChar
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
-	DWordToChar
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongToChar function


## -description


Converts a value of type <b>DWORD</b> to a value of type <b>CHAR</b>.


## -parameters




### -param ulOperand

TBD


### -param pch [out]

Type: <b>__wchar_t*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - dwOperand [in]

Type: <b>DWORD</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



