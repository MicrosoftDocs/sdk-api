---
UID: NF:intsafe.ULongAdd
title: ULongAdd function
author: windows-driver-content
description: Adds two values of type DWORD.
old-location: shell\DWordAdd.htm
old-project: shell
ms.assetid: d99e262f-7f04-472c-898b-9ca63a4d2448
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: DWordAdd, DWordAdd function [Windows Shell], ULongAdd, _shell_DWordAdd, intsafe/DWordAdd, shell.DWordAdd
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
-	DWordAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongAdd function


## -description


Adds two values of type <b>DWORD</b>.


## -parameters




### -param ulAugend

TBD


### -param ulAddend

TBD


### -param pulResult

TBD




#### - dwAddend [in]

Type: <b>DWORD</b>

The value to add to <i>dwAugend</i>.


#### - dwAugend [in]

Type: <b>DWORD</b>

The first value in the equation.


#### - pdwResult [out]

Type: <b>DWORD*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



