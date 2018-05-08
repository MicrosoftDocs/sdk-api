---
UID: NF:intsafe.IntToUInt8
title: IntToUInt8 function
author: windows-driver-content
description: Converts a value of type INT to a value of type BYTE.
old-location: shell\IntToByte.htm
old-project: shell
ms.assetid: 12be7a22-b8f1-4d7a-bf16-6f70adfcda32
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IntToByte, IntToByte function [Windows Shell], IntToUInt8, _shell_IntToByte, intsafe/IntToByte, shell.IntToByte
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
-	IntToByte
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntToUInt8 function


## -description


Converts a value of type <b>INT</b> to a value of type <b>BYTE</b>.


## -parameters




### -param iOperand [in]

Type: <b>INT</b>

The value to be converted.


### -param pui8Result

TBD




#### - pb [out]

Type: <b>BYTE*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



