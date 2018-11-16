---
UID: NF:intsafe.LongToUInt8
title: LongToUInt8 function
author: windows-sdk-content
description: Converts a value of type LONG to a value of type UINT8.
old-location: shell\LongToUInt8.htm
tech.root: shell
ms.assetid: 46b20b7c-f822-4521-8598-73193da67d2c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LongToByte, LongToUInt8, LongToUInt8 function [Windows Shell], intsafe/LongToUInt8, shell.LongToUInt8
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - intsafe.h
api_name:
 - LongToUInt8
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LongToUInt8
: 
---

# LongToUInt8 function


## -description


Converts a value of type <b>LONG</b> to a value of type <b>UINT8</b>.


## -parameters




### -param lOperand [in]

The value to convert.


### -param pui8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of functions designed to provide type conversions and perform validity checks with minimal impact on performance.

<b>LongToByte</b> is an alias for this function.



