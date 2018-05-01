---
UID: NF:intsafe.ShortToUInt8
title: ShortToUInt8 function
author: windows-driver-content
description: Converts a value of type SHORT to a value of type BYTE.
old-location: shell\ShortToByte.htm
old-project: shell
ms.assetid: 71bd9691-0733-47ba-bea3-0779c6bad253
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ShortToByte, ShortToByte function [Windows Shell], ShortToUInt8, _shell_ShortToByte, intsafe/ShortToByte, shell.ShortToByte
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
-	ShortToByte
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ShortToUInt8 function


## -description


Converts a value of type <b>SHORT</b> to a value of type <b>BYTE</b>.


## -parameters




### -param sOperand [in]

Type: <b>SHORT</b>

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



