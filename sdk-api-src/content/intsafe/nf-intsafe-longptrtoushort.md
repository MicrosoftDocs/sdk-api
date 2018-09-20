---
UID: NF:intsafe.LongPtrToUShort
title: LongPtrToUShort function
author: windows-sdk-content
description: Converts a value of type LONG_PTR to a value of type USHORT.
old-location: shell\LongPtrToUShort.htm
tech.root: shell
ms.assetid: d20be0c8-f228-4fed-847b-d28d99ade476
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: LongPtrToUShort, LongPtrToUShort function [Windows Shell], intsafe/LongPtrToUShort, shell.LongPtrToUShort
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
 - LongPtrToUShort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LongPtrToUShort function


## -description


Converts a value of type <b>LONG_PTR</b> to a value of type <b>USHORT</b>.


## -parameters




### -param lOperand [in]

The value to convert.


### -param pusResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



