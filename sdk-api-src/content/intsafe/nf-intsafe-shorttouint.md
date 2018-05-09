---
UID: NF:intsafe.ShortToUInt
title: ShortToUInt function
author: windows-driver-content
description: Converts a value of type SHORT to a value of type UINT.
old-location: shell\ShortToUInt.htm
old-project: shell
ms.assetid: e00b9dd2-fa40-401b-9002-e65c91d2b6ef
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ShortToUInt, ShortToUInt function [Windows Shell], intsafe/ShortToUInt, shell.ShortToUInt
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
-	ShortToUInt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ShortToUInt function


## -description


Converts a value of type <b>SHORT</b> to a value of type <b>UINT</b>.


## -parameters




### -param sOperand [in]

The value to convert.


### -param puResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



