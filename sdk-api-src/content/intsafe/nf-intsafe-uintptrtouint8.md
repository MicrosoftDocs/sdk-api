---
UID: NF:intsafe.UIntPtrToUInt8
title: UIntPtrToUInt8 function
author: windows-driver-content
description: Converts a value of type UINT_PTR to a value of type UINT8.
old-location: shell\UIntPtrToUInt8.htm
old-project: shell
ms.assetid: 5490bca2-52c8-4e98-a2ac-137aa7c423de
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: UIntPtrToUInt8, UIntPtrToUInt8 function [Windows Shell], intsafe/UIntPtrToUInt8, shell.UIntPtrToUInt8
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
-	UIntPtrToUInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToUInt8 function


## -description


Converts a value of type <b>UINT_PTR</b> to a value of type <b>UINT8</b>.


## -parameters




### -param uOperand [in]

The value to convert.


### -param pu8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



