---
UID: NF:intsafe.ULongToLong
title: ULongToLong function
author: windows-driver-content
description: Converts a value of type DWORD to a value of type LONG.
old-location: shell\DWordToLong.htm
old-project: shell
ms.assetid: 885566bf-cbc6-4f26-9869-fdefbd360ff2
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DWordToLong, DWordToLong function [Windows Shell], ULongToLong, _shell_DWordToLong, intsafe/DWordToLong, shell.DWordToLong
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
-	DWordToLong
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongToLong function


## -description


Converts a value of type <b>DWORD</b> to a value of type <b>LONG</b>.


## -parameters




### -param ulOperand

TBD


### -param plResult [out]

Type: <b>LONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - dwOperand [in]

Type: <b>DWORD</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



