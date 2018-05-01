---
UID: NF:intsafe.IntPtrToULong
title: IntPtrToULong function
author: windows-driver-content
description: Converts a value of type INT_PTR to a value of type DWORD.
old-location: shell\IntPtrToDWord.htm
old-project: shell
ms.assetid: 886758e5-9316-4286-be60-4af4e37ac2eb
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IntPtrToDWord, IntPtrToDWord function [Windows Shell], IntPtrToULong, _shell_IntPtrToDWord, intsafe/IntPtrToDWord, shell.IntPtrToDWord
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
-	IntPtrToDWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntPtrToULong function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>DWORD</b>.


## -parameters




### -param iOperand [in]

Type: <b>INT_PTR</b>

The value to be converted.


### -param pulResult

TBD




#### - pdwResult [out]

Type: <b>DWORD*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



