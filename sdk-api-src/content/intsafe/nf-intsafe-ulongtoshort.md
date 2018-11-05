---
UID: NF:intsafe.ULongToShort
title: ULongToShort function
author: windows-sdk-content
description: Converts a value of type ULONG to a value of type SHORT.
old-location: shell\ULongToShort.htm
tech.root: shell
ms.assetid: e6af3c05-03e3-4c55-9730-710fe282dbf3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DWordToShort, ULongToShort, ULongToShort function [Windows Shell], _shell_ULongToShort, intsafe/ULongToShort, shell.ULongToShort
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - ULongToShort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ULongToShort function


## -description


Converts a value of type <b>ULONG</b> to a value of type <b>SHORT</b>.


## -parameters




### -param ulOperand [in]

Type: <b>ULONG</b>

The value to be converted.


### -param psResult [out]

Type: <b>SHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>DWordToShort</b> is an alias for this function.



