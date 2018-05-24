---
UID: NF:intsafe.ULongPtrToChar
title: ULongPtrToChar function
author: windows-driver-content
description: Converts a value of type ULONG_PTR to a value of type CHAR.
old-location: shell\ULongPtrToChar.htm
old-project: shell
ms.assetid: 0cc26423-5c14-49d0-984e-f2bb81f68010
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ULongPtrToChar, ULongPtrToChar function [Windows Shell], intsafe/ULongPtrToChar, shell.ULongPtrToChar
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
-	ULongPtrToChar
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongPtrToChar function


## -description


Converts a value of type <b>ULONG_PTR</b> to a value of type <b>CHAR</b>.


## -parameters




### -param ulOperand [in]

The value to convert.


### -param pch [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



