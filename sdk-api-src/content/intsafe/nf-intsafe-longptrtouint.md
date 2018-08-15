---
UID: NF:intsafe.LongPtrToUInt
title: LongPtrToUInt function
author: windows-sdk-content
description: Converts a value of type LONG_PTR to a value of type UINT.
old-location: shell\LongPtrToUInt.htm
old-project: shell
ms.assetid: b738dfcf-6c99-4795-9d9a-6b2349429140
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LongPtrToUInt, LongPtrToUInt function [Windows Shell], SSIZETToUInt, _shell_LongPtrToUInt, intsafe/LongPtrToUInt, shell.LongPtrToUInt
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
 - LongPtrToUInt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongPtrToUInt function


## -description


Converts a value of type <b>LONG_PTR</b> to a value of type <b>UINT</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG_PTR</b>

The value to be converted.


### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>SSIZETToUInt</b> is an alias for this function.



