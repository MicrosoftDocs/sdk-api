---
UID: NF:intsafe.LongLongToUInt8
title: LongLongToUInt8 function
author: windows-driver-content
description: Converts a value of type LONGLONG to a value of type UINT8.
old-location: shell\LongLongToUInt8.htm
old-project: shell
ms.assetid: b8dd8478-7c15-4183-9531-dd06ea2ccb03
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: LongLongToUInt8, LongLongToUInt8 function [Windows Shell], intsafe/LongLongToUInt8, shell.LongLongToUInt8
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
-	LongLongToUInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToUInt8 function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>UINT8</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param pu8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



