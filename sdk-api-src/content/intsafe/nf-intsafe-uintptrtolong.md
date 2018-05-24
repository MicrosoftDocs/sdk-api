---
UID: NF:intsafe.UIntPtrToLong
title: UIntPtrToLong function
author: windows-driver-content
description: Converts a value of type size_t to a value of type LONG.
old-location: shell\SizeTToLong.htm
old-project: shell
ms.assetid: 1904fefa-eb31-4fda-ad0b-8ad6d2b62210
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: SizeTToLong, SizeTToLong function [Windows Shell], UIntPtrToLong, _shell_SizeTToLong, intsafe/SizeTToLong, shell.SizeTToLong
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
-	SizeTToLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToLong function


## -description


Converts a value of type <b>size_t</b> to a value of type <b>LONG</b>.


## -parameters




### -param uOperand

TBD


### -param plResult [out]

Type: <b>LONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - cbOperand [in]

Type: <b>size_t</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



