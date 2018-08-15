---
UID: NF:intsafe.ShortToChar
title: ShortToChar function
author: windows-sdk-content
description: Converts a value of type SHORT to a value of CHAR.
old-location: shell\ShortToChar.htm
old-project: shell
ms.assetid: 5037b473-d8d3-41f0-80f2-4633ae6a8321
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ShortToChar, ShortToChar function [Windows Shell], _shell_ShortToChar, intsafe/ShortToChar, shell.ShortToChar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.redist: 
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
 - ShortToChar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ShortToChar function


## -description


Converts a value of type <b>SHORT</b> to a value of <b>CHAR</b>.


## -parameters




### -param sOperand [in]

Type: <b>SHORT</b>

The value to be converted.


### -param pch [out]

Type: <b>__wchar_t*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



