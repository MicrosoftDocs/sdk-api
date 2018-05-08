---
UID: NF:intsafe.ULongPtrToIntPtr
title: ULongPtrToIntPtr function
author: windows-driver-content
description: Converts a value of type DWORD_PTR to a value of type INT_PTR.
old-location: shell\DWordPtrToIntPtr.htm
old-project: shell
ms.assetid: 8d3931b4-c44f-416f-97f4-911f78861fb5
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: DWordPtrToIntPtr, DWordPtrToIntPtr function [Windows Shell], ULongPtrToIntPtr, _shell_DWordPtrToIntPtr, intsafe/DWordPtrToIntPtr, shell.DWordPtrToIntPtr
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
-	DWordPtrToIntPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongPtrToIntPtr function


## -description


Converts a value of type <b>DWORD_PTR</b> to a value of type <b>INT_PTR</b>.


## -parameters




### -param ulOperand

TBD


### -param piResult [out]

Type: <b>INT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


#### - dwOperand [in]

Type: <b>DWORD_PTR</b>

The value to be converted.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



