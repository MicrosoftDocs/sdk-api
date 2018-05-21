---
UID: NF:intsafe.LongPtrAdd
title: LongPtrAdd function
author: windows-driver-content
description: Adds two values of type LONG_PTR.
old-location: shell\LongPtrAdd.htm
old-project: shell
ms.assetid: 1c5f3112-12f1-409f-9a0f-74d4d35abb48
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: LongPtrAdd, LongPtrAdd function [Windows Shell], intsafe/LongPtrAdd, shell.LongPtrAdd
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	LongPtrAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongPtrAdd function


## -description


Adds two values of type <b>LONG_PTR</b>.


## -parameters




### -param lAugend [in]

The first value.


### -param lAddend [in]

The second value.


### -param plResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



