---
UID: NF:intsafe.ULongLongToUIntPtr
title: ULongLongToUIntPtr function
author: windows-driver-content
description: Converts a value of type ULONGLONG to a value of type size_t.
old-location: shell\ULongLongToSizeT.htm
old-project: shell
ms.assetid: 8943b23b-946e-477a-a5d2-ff2d877db73f
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ULongLongToSizeT, ULongLongToSizeT function [Windows Shell], ULongLongToUIntPtr, _shell_ULongLongToSizeT, intsafe/ULongLongToSizeT, shell.ULongLongToSizeT
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
-	ULongLongToSizeT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongToUIntPtr function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>size_t</b>.


## -parameters




### -param ullOperand [in]

Type: <b>ULONGLONG</b>

The value to be converted.


### -param puResult

TBD




#### - pcbResult [out]

Type: <b>size_t*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



