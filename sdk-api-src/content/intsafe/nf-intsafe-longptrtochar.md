---
UID: NF:intsafe.LongPtrToChar
title: LongPtrToChar function
author: windows-driver-content
description: Converts a value of type LONG_PTR to a value of type CHAR.
old-location: shell\LongPtrToChar.htm
old-project: shell
ms.assetid: 661b7a6f-5524-44e5-9999-61c9df8e7cd3
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: LongPtrToChar, LongPtrToChar function [Windows Shell], intsafe/LongPtrToChar, shell.LongPtrToChar
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
-	LongPtrToChar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongPtrToChar function


## -description


Converts a value of type <b>LONG_PTR</b> to a value of type <b>CHAR</b>.


## -parameters




### -param lOperand [in]

The value to convert.


### -param pch [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



