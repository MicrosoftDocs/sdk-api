---
UID: NF:intsafe.LongLongToShort
title: LongLongToShort function
author: windows-driver-content
description: Converts a value of type LONGLONG to a value of type SHORT.
old-location: shell\LongLongToShort.htm
old-project: shell
ms.assetid: c292f2f0-18c3-4675-8ff9-8c773aa6dc8e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: LongLongToShort, LongLongToShort function [Windows Shell], intsafe/LongLongToShort, shell.LongLongToShort
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
-	LongLongToShort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToShort function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>SHORT</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param psResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



