---
UID: NF:intsafe.ULongToUChar
title: ULongToUChar function
author: windows-driver-content
description: Converts a value of type DWORD to a value of type UCHAR.
old-location: shell\DWordToUChar.htm
old-project: shell
ms.assetid: 1299608f-782b-4492-8b92-41eb72d93c17
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: DWordToUChar, DWordToUChar function [Windows Shell], ULongToUChar, _shell_DWordToUChar, intsafe/DWordToUChar, shell.DWordToUChar
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
-	DWordToUChar
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongToUChar function


## -description


Converts a value of type <b>DWORD</b> to a value of type <b>UCHAR</b>.


## -parameters




### -param ulOperand

TBD


### -param pch

TBD




#### - dwOperand [in]

Type: <b>DWORD</b>

The value to be converted.


#### - puchResult [out]

Type: <b>UCHAR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



