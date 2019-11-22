---
UID: NF:intsafe.IntToUChar
title: IntToUChar function (intsafe.h)

description: Converts a value of type INT to a value of type UCHAR.
old-location: shell\IntToUChar.htm
tech.root: shell
ms.assetid: 19bdf34e-49ae-4dff-bed7-fa6229c8aa1b

ms.date: 12/05/2018
ms.keywords: IntToUChar, IntToUChar function [Windows Shell], _shell_IntToUChar, intsafe/IntToUChar, shell.IntToUChar
ms.topic: function
f1_keywords: 
 - "intsafe/IntToUChar"
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
 - IntToUChar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IntToUChar function


## -description


Converts a value of type <b>INT</b> to a value of type <b>UCHAR</b>.


## -parameters




### -param iOperand [in]

Type: <b>INT</b>

The value to be converted.


### -param pch [out]

Type: <b>UCHAR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



