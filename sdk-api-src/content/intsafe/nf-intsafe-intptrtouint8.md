---
UID: NF:intsafe.IntPtrToUInt8
title: IntPtrToUInt8 function
author: windows-sdk-content
description: Converts a value of type INT_PTR to a value of type UINT8.
old-location: shell\IntPtrToUInt8.htm
tech.root: shell
ms.assetid: d1337a8a-0a7a-41a1-b57b-f20d8a616113
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IntPtrToUInt8, IntPtrToUInt8 function [Windows Shell], intsafe/IntPtrToUInt8, shell.IntPtrToUInt8
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
 - IntPtrToUInt8
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntPtrToUInt8 function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>UINT8</b>.


## -parameters




### -param iOperand [in]

The value to convert.


### -param pui8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



