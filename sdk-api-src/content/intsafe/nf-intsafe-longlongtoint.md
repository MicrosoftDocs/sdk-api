---
UID: NF:intsafe.LongLongToInt
title: LongLongToInt function
author: windows-sdk-content
description: Converts a value of type LONGLONG to a value of type INT.
old-location: shell\LongLongToInt.htm
old-project: shell
ms.assetid: c011e0d1-69bd-446b-a352-ef92dd801f2e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Int64ToInt, LongLongToInt, LongLongToInt function [Windows Shell], intsafe/LongLongToInt, shell.LongLongToInt
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
-	LongLongToInt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToInt function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>INT</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param piResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Int64ToInt</b> is an alias for this function.



