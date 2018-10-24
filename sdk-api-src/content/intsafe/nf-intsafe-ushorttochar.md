---
UID: NF:intsafe.UShortToChar
title: UShortToChar function
author: windows-sdk-content
description: Converts a value of type USHORT to a value of type CHAR.
old-location: shell\UShortToChar.htm
tech.root: shell
ms.assetid: 9d5b57a8-7b5b-4a40-a022-57149fec76de
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: UShortToChar, UShortToChar function [Windows Shell], WordToChar, _shell_UShortToChar, intsafe/UShortToChar, shell.UShortToChar
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
 - UShortToChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UShortToChar function


## -description


Converts a value of type <b>USHORT</b> to a value of type <b>CHAR</b>.


## -parameters




### -param usOperand [in]

Type: <b>USHORT</b>

The value to be converted.


### -param pch [out]

Type: <b>__wchar_t*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>WordToChar</b> is an alias for this function.



