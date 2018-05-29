---
UID: NF:intsafe.IntSub
title: IntSub function
author: windows-sdk-content
description: Subtracts one value of type INT from another.
old-location: shell\IntSub.htm
old-project: shell
ms.assetid: ee083a68-27fd-4c94-93e0-7e662c48d5cf
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IntSub, IntSub function [Windows Shell], intsafe/IntSub, shell.IntSub
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
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	intsafe.h
api_name:
-	IntSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntSub function


## -description


Subtracts one value of type <b>INT</b> from another.


## -parameters




### -param iMinuend [in]

The first value.


### -param iSubtrahend [in]

The value to subtract.


### -param piResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



