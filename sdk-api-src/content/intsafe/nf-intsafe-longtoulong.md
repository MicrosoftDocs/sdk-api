---
UID: NF:intsafe.LongToULong
title: LongToULong function
author: windows-sdk-content
description: Converts a value of type LONG to a value of type ULONG.
old-location: shell\LongToULong.htm
tech.root: shell
ms.assetid: d5940fec-8cf2-4bc7-8001-42b68ce97f7d
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: LongToDWord, LongToULong, LongToULong function [Windows Shell], _shell_LongToULong, intsafe/LongToULong, shell.LongToULong
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
 - LongToULong
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LongToULong function


## -description


Converts a value of type <b>LONG</b> to a value of type <b>ULONG</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.


### -param pulResult [out]

Type: <b>ULONG*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>LongToDWord</b> is an alias for this function.



