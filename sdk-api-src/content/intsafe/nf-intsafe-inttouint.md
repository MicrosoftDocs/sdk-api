---
UID: NF:intsafe.IntToUInt
title: IntToUInt function
author: windows-sdk-content
description: Converts a value of type INT to a value of type UINT.
old-location: shell\IntToUInt.htm
tech.root: shell
ms.assetid: 54fe3370-648a-40ab-856b-d34c0c033141
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IntToUInt, IntToUInt function [Windows Shell], _shell_IntToUInt, intsafe/IntToUInt, shell.IntToUInt
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
 - IntToUInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntToUInt function


## -description


Converts a value of type <b>INT</b> to a value of type <b>UINT</b>.


## -parameters




### -param iOperand [in]

Type: <b>INT</b>

The value to be converted.


### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



