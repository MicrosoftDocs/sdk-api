---
UID: NF:intsafe.IntPtrToChar
title: IntPtrToChar function
author: windows-driver-content
description: Converts a value of type INT_PTR to a value of type CHAR.
old-location: shell\IntPtrToChar.htm
old-project: shell
ms.assetid: e0f8139e-9d40-4fac-a08b-651909b0a567
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IntPtrToChar, IntPtrToChar function [Windows Shell], intsafe/IntPtrToChar, shell.IntPtrToChar
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
-	IntPtrToChar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntPtrToChar function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>CHAR</b>.


## -parameters




### -param iOperand [in]

The value to convert.


### -param pch [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



