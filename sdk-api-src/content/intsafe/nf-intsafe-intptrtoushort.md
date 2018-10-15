---
UID: NF:intsafe.IntPtrToUShort
title: IntPtrToUShort function
author: windows-sdk-content
description: Converts a value of type INT_PTR to a value of type USHORT.
old-location: shell\IntPtrToUShort.htm
tech.root: shell
ms.assetid: c1ab8cbc-0c45-410c-a34d-2bded36a03e8
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IntPtrToUShort, IntPtrToUShort function [Windows Shell], intsafe/IntPtrToUShort, shell.IntPtrToUShort
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
 - IntPtrToUShort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntPtrToUShort function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>USHORT</b>.


## -parameters




### -param iOperand [in]

The value to convert.


### -param pusResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



