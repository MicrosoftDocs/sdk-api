---
UID: NF:intsafe.UIntToUShort
title: UIntToUShort function
author: windows-sdk-content
description: Converts a value of type UINT to a value of type USHORT.
old-location: shell\UIntToUShort.htm
tech.root: shell
ms.assetid: 3328c24d-e576-4b57-a03f-506bc172ac2c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: UIntToUShort, UIntToUShort function [Windows Shell], UIntToWord, _shell_UIntToUShort, intsafe/UIntToUShort, shell.UIntToUShort
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
 - UIntToUShort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UIntToUShort function


## -description


Converts a value of type <b>UINT</b> to a value of type <b>USHORT</b>.


## -parameters




### -param uOperand [in]

Type: <b>UINT</b>

The value to be converted.


### -param pusResult [out]

Type: <b>USHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>UIntToWord</b> is an alias for this function.



