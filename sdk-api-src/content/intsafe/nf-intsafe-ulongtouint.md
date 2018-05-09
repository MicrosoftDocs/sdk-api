---
UID: NF:intsafe.ULongToUInt
title: ULongToUInt function
author: windows-driver-content
description: Converts a value of type DWORD to a value of type UINT.
old-location: shell\DWordToUInt.htm
old-project: shell
ms.assetid: 93198910-c683-496a-b273-b38dff9e4463
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DWordToUInt, DWordToUInt function [Windows Shell], ULongToUInt, _shell_DWordToUInt, intsafe/DWordToUInt, shell.DWordToUInt
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
-	DWordToUInt
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongToUInt function


## -description


Converts a value of type <b>DWORD</b> to a value of type <b>UINT</b>.


## -parameters




### -param ulOperand

TBD


### -param puResult

TBD




#### - dwOperand [in]

Type: <b>DWORD</b>

The value to be converted.


#### - puiResult [out]

Type: <b>UINT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



