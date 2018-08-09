---
UID: NF:intsafe.LongPtrSub
title: LongPtrSub function
author: windows-sdk-content
description: Subtracts one value of type LONG_PTR from another.
old-location: shell\LongPtrSub.htm
old-project: shell
ms.assetid: f6e35f6a-9af1-4e14-82c0-0f96ecf01c15
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LongPtrSub, LongPtrSub function [Windows Shell], intsafe/LongPtrSub, shell.LongPtrSub
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - LongPtrSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongPtrSub function


## -description


Subtracts one value of type <b>LONG_PTR</b> from another.


## -parameters




### -param lMinuend [in]

The first value.


### -param lSubtrahend [in]

The value to subtract.


### -param plResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



