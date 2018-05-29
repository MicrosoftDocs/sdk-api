---
UID: NF:intsafe.LongToIntPtr
title: LongToIntPtr function
author: windows-sdk-content
description: Converts a value of type LONG to a value of type INT_PTR.
old-location: shell\LongToIntPtr.htm
old-project: shell
ms.assetid: 6ec7c2fa-3e29-4c61-a81f-12aa5d52f3f0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: LongToIntPtr, LongToIntPtr function [Windows Shell], LongToPtrdiffT, _shell_LongToIntPtr, intsafe/LongToIntPtr, shell.LongToIntPtr
ms.prod: windows
ms.technology: windows-sdk
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
-	LongToIntPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongToIntPtr function


## -description


Converts a value of type <b>LONG</b> to a value of type <b>INT_PTR</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.


### -param piResult [out]

Type: <b>INT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>LongToPtrdiffT</b> is an alias for this function.



