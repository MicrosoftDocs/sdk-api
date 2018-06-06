---
UID: NF:intsafe.IntPtrSub
title: IntPtrSub function
author: windows-sdk-content
description: Subtracts one value of type INT_PTR from another.
old-location: shell\IntPtrSub.htm
old-project: shell
ms.assetid: ad30f236-7412-401f-b6a9-76b74118092d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IntPtrSub, IntPtrSub function [Windows Shell], intsafe/IntPtrSub, shell.IntPtrSub
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
 - IntPtrSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



