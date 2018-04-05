---
UID: NF:intsafe.ULongPtrToUInt8
title: ULongPtrToUInt8 function
author: windows-driver-content
description: Converts a value of type ULONG_PTR to a value of type UINT8.
old-location: shell\ULongPtrToUInt8.htm
old-project: shell
ms.assetid: 1a287c22-80d8-4cd9-8878-c19aaeddd407
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ULongPtrToUInt8, ULongPtrToUInt8 function [Windows Shell], intsafe/ULongPtrToUInt8, shell.ULongPtrToUInt8
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
-	ULongPtrToUInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongPtrToUInt8 function


## -description


Converts a value of type <b>ULONG_PTR</b> to a value of type <b>UINT8</b>.


## -parameters




### -param ulOperand [in]

The value to convert.


### -param pui8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



