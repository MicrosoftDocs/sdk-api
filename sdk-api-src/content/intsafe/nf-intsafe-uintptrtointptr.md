---
UID: NF:intsafe.UIntPtrToIntPtr
title: UIntPtrToIntPtr function
author: windows-driver-content
description: Converts a value of type size_t to a value of type INT_PTR.
old-location: shell\SizeTToIntPtr.htm
old-project: shell
ms.assetid: 91e7119f-deac-4a72-8071-b92b031a311e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SizeTToIntPtr, SizeTToIntPtr function [Windows Shell], UIntPtrToIntPtr, _shell_SizeTToIntPtr, intsafe/SizeTToIntPtr, shell.SizeTToIntPtr
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
-	SizeTToIntPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToIntPtr function


## -description


Converts a value of type <b>size_t</b> to a value of type <b>INT_PTR</b>.


## -parameters




### -param uOperand

TBD


### -param piResult [out]

Type: <b>INT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - cbOperand [in]

Type: <b>size_t</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



