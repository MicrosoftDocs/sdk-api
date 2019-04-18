---
UID: NF:intsafe.LongToChar
title: LongToChar function (intsafe.h)
author: windows-sdk-content
description: Converts a value of type LONG to a value of type CHAR.
old-location: shell\LongToChar.htm
tech.root: shell
ms.assetid: 1abf1466-3491-4719-8dd2-82e4ba2506c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LongToChar, LongToChar function [Windows Shell], _shell_LongToChar, intsafe/LongToChar, shell.LongToChar
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
 - LongToChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LongToChar function


## -description


Converts a value of type <b>LONG</b> to a value of type <b>CHAR</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.


### -param pch [out]

Type: <b>__wchar_t*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



