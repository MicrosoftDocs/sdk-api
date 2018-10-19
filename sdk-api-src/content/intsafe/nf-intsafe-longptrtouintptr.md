---
UID: NF:intsafe.LongPtrToUIntPtr
title: LongPtrToUIntPtr function
author: windows-sdk-content
description: Converts a value of type LONG_PTR to a value of type UINT_PTR.
old-location: shell\LongPtrToUIntPtr.htm
tech.root: shell
ms.assetid: f2f554ba-b26d-4ee9-9a43-4814c661c7c4
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: LongPtrToSizeT, LongPtrToUIntPtr, LongPtrToUIntPtr function [Windows Shell], SSIZETToSizeT, _shell_LongPtrToUIntPtr, intsafe/LongPtrToUIntPtr, shell.LongPtrToUIntPtr
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
 - LongPtrToUIntPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LongPtrToUIntPtr function


## -description


Converts a value of type <b>LONG_PTR</b> to a value of type <b>UINT_PTR</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG_PTR</b>

The value to be converted.


### -param puResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>LongPtrToSizeT</b> is an alias for this function.

<b>SSIZETToSizeT</b> is an alias for this function.



