---
UID: NF:intsafe.LongToInt8
title: LongToInt8 function
author: windows-driver-content
description: Converts a value of type LONG to a value of type INT8.
old-location: shell\LongToInt8.htm
old-project: shell
ms.assetid: 611dd8dc-4aac-4efd-aa7d-9dd1867219cc
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: LongToInt8, LongToInt8 function [Windows Shell], intsafe/LongToInt8, shell.LongToInt8
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
-	LongToInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongToInt8 function


## -description


Converts a value of type <b>LONG</b> to a value of type <b>INT8</b>.


## -parameters




### -param lOperand [in]

The value to convert.


### -param pi8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



