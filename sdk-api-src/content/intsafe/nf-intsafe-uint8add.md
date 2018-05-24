---
UID: NF:intsafe.UInt8Add
title: UInt8Add function
author: windows-driver-content
description: Adds two values of type UINT8.
old-location: shell\UInt8Add.htm
old-project: shell
ms.assetid: 576be346-55bc-41a7-93d3-612b6ef8a267
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: UInt8Add, UInt8Add function [Windows Shell], intsafe/UInt8Add, shell.UInt8Add
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
-	UInt8Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UInt8Add function


## -description


Adds two values of type <b>UINT8</b>.


## -parameters




### -param u8Augend [in]

The first value.


### -param u8Addend [in]

The second value.


### -param pu8Result [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



