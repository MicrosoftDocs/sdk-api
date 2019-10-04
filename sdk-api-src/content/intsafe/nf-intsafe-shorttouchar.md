---
UID: NF:intsafe.ShortToUChar
title: ShortToUChar function (intsafe.h)
author: windows-sdk-content
description: Converts a value of type SHORT to a value of UCHAR.
old-location: shell\ShortToUChar.htm
tech.root: shell
ms.assetid: dd3eab34-7cf1-4a60-8fd8-bcc9db1855d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ShortToUChar, ShortToUChar function [Windows Shell], _shell_ShortToUChar, intsafe/ShortToUChar, shell.ShortToUChar
ms.topic: function
f1_keywords: 
 - "intsafe/ShortToUChar"
dev_langs:
 - c++
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
 - ShortToUChar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ShortToUChar function


## -description


Converts a value of type <b>SHORT</b> to a value of <b>UCHAR</b>.


## -parameters




### -param sOperand [in]

Type: <b>SHORT</b>

The value to be converted.


### -param pch [out]

Type: <b>UCHAR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



