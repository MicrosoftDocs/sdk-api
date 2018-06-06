---
UID: NF:intsafe.ULongToUInt
title: ULongToUInt function
author: windows-sdk-content
description: Converts a value of type ULONG to a value of type UINT.
old-location: shell\ULongToUInt.htm
old-project: shell
ms.assetid: f3e11789-9fea-41f6-9d96-ac0a7e267e7e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DWordToUInt, ULongToUInt, ULongToUInt function [Windows Shell], _shell_ULongToUInt, intsafe/ULongToUInt, shell.ULongToUInt
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - ULongToUInt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongToUInt function


## -description


Converts a value of type <b>ULONG</b> to a value of type <b>UINT</b>.


## -parameters




### -param ulOperand [in]

Type: <b>ULONG</b>

The value to be converted.


### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>DWordToUInt</b> is an alias for this function.



