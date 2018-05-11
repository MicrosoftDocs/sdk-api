---
UID: NF:intsafe.LongLongToInt
title: LongLongToInt function
author: windows-driver-content
description: Converts a value of type INT64 to a value of type INT.
old-location: shell\Int64ToInt.htm
old-project: shell
ms.assetid: 3d652b20-35d7-4e37-a1c8-de4a91eebd93
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Int64ToInt, Int64ToInt function [Windows Shell], LongLongToInt, _shell_Int64ToInt, intsafe/Int64ToInt, shell.Int64ToInt
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
-	Int64ToInt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToInt function


## -description


Converts a value of type <b>INT64</b> to a value of type <b>INT</b>.


## -parameters




### -param llOperand

TBD


### -param piResult [out]

Type: <b>INT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - i64Operand [in]

Type: <b>INT64</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



