---
UID: NF:intsafe.ULongLongToLongLong
title: ULongLongToLongLong function
author: windows-driver-content
description: Converts a value of type ULONGLONG to a value of type LONGLONG.
old-location: shell\ULongLongToLongLong.htm
old-project: shell
ms.assetid: c95eb6f6-f179-4471-a185-ebc8c634b2c3
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ULongLongToLongLong, ULongLongToLongLong function [Windows Shell], intsafe/ULongLongToLongLong, shell.ULongLongToLongLong
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
-	ULongLongToLongLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongToLongLong function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>LONGLONG</b>.


## -parameters




### -param ullOperand [in]

The value to convert.


### -param pllResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



