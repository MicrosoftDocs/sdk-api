---
UID: NF:intsafe.LongLongAdd
title: LongLongAdd function
author: windows-driver-content
description: Adds two values of type LONGLONG.
old-location: shell\LongLongAdd.htm
old-project: shell
ms.assetid: b3010519-583e-4341-a673-9cc97a6f4232
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: LongLongAdd, LongLongAdd function [Windows Shell], intsafe/LongLongAdd, shell.LongLongAdd
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
-	LongLongAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongAdd function


## -description


Adds two values of type <b>LONGLONG</b>.


## -parameters




### -param llAugend [in]

The first value.


### -param llAddend [in]

The second value.


### -param pllResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



