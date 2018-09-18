---
UID: NF:intsafe.LongLongToULong
title: LongLongToULong function
author: windows-sdk-content
description: Converts a value of type LONGLONG to a value of type ULONG.
old-location: shell\LongLongToULong.htm
tech.root: shell
ms.assetid: b816c07a-d257-4c2c-b3a7-958c763111ca
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: DWordToUShort, Int64ToDWordPtr, Int64ToSIZET, Int64ToULong, IntPtrToULong, LongLongToULong, LongLongToULong function [Windows Shell], intsafe/LongLongToULong, shell.LongLongToULong
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
 - LongLongToULong
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LongLongToULong function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>ULONG</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param pulResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Int64ToULong</b> is an alias for this function.

<b>Int64ToSIZET</b> is an alias for this function.

<b>Int64ToDWordPtr</b> is an alias for this function.

<b>IntPtrToULong</b> is an alias for this function.

<b>DWordToUShort</b> is an alias for this function.



