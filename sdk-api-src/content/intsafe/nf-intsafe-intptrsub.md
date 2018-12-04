---
UID: NF:intsafe.IntPtrSub
title: IntPtrSub function
author: windows-sdk-content
description: Subtracts one value of type INT_PTR from another.
old-location: shell\IntPtrSub.htm
tech.root: shell
ms.assetid: ad30f236-7412-401f-b6a9-76b74118092d
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IntPtrSub, IntPtrSub function [Windows Shell], intsafe/IntPtrSub, shell.IntPtrSub
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
 - IntPtrSub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntPtrSub function


## -description


Subtracts one value of type <b>INT_PTR</b> from another.


## -parameters




### -param iMinuend [in]

The first value.


### -param iSubtrahend [in]

The value to subtract.


### -param piResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



