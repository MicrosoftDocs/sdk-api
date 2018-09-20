---
UID: NF:intsafe.LongLongToUChar
title: LongLongToUChar function
author: windows-sdk-content
description: Converts a value of type LONGLONG to a value of type UCHAR.
old-location: shell\LongLongToUChar.htm
tech.root: shell
ms.assetid: 5c8440fa-aefe-4f63-877c-4b1ebdc59138
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: LongLongToUChar, LongLongToUChar function [Windows Shell], intsafe/LongLongToUChar, shell.LongLongToUChar
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
 - LongLongToUChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LongLongToUChar function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>UCHAR</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param pch [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



