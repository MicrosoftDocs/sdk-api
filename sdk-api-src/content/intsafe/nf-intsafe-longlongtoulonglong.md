---
UID: NF:intsafe.LongLongToULongLong
title: LongLongToULongLong function
author: windows-driver-content
description: Converts a value of type LONGLONG to a value of type ULONGLONG.
old-location: shell\LongLongToULongLong.htm
old-project: shell
ms.assetid: 994f0b9f-77a6-41ef-9022-a26ef5660204
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: LongLongToULongLong, LongLongToULongLong function [Windows Shell], intsafe/LongLongToULongLong, shell.LongLongToULongLong
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
-	LongLongToULongLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToULongLong function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>ULONGLONG</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param pullResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



