---
UID: NF:intsafe.UIntToLongPtr
title: UIntToLongPtr function
author: windows-sdk-content
description: Converts a value of type UINT to a value of type LONG_PTR.
old-location: shell\UIntToLongPtr.htm
tech.root: shell
ms.assetid: bf26b6da-ecc6-4ee0-9da8-54fa0261427a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: UIntToLongPtr, UIntToLongPtr function [Windows Shell], UIntToSSIZET, _shell_UIntToLongPtr, intsafe/UIntToLongPtr, shell.UIntToLongPtr
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
 - UIntToLongPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UIntToLongPtr function


## -description


Converts a value of type <b>UINT</b> to a value of type <b>LONG_PTR</b>.


## -parameters




### -param uOperand [in]

Type: <b>UINT</b>

The value to be converted.


### -param plResult [out]

Type: <b>LONGPTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>UIntToSSIZET</b> is an alias for this function.



