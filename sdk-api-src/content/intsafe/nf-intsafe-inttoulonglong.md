---
UID: NF:intsafe.IntToULongLong
title: IntToULongLong function
author: windows-sdk-content
description: Converts a value of type INT to a value of type UINT_PTR.
old-location: shell\IntToUIntPtr.htm
tech.root: shell
ms.assetid: 479958f6-e38c-404c-b4bd-2991be568a2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IntToUIntPtr, IntToUIntPtr function [Windows Shell], IntToULongLong, _shell_IntToUIntPtr, intsafe/IntToUIntPtr, shell.IntToUIntPtr
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
 - IntToUIntPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntToULongLong function


## -description


Converts a value of type <b>INT</b> to a value of type <b>UINT_PTR</b>.


## -parameters




### -param iOperand [in]

Type: <b>INT</b>

The value to be converted.


### -param pullResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the address of the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



