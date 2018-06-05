---
UID: NF:intsafe.UIntPtrToInt8
title: UIntPtrToInt8 function
author: windows-sdk-content
description: Converts a value of type UINT_PTR to a value of type INT8.
old-location: shell\UIntPtrToInt8.htm
old-project: shell
ms.assetid: fd421216-e2c3-453f-8dd0-0a904a2e0c31
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: UIntPtrToInt8, UIntPtrToInt8 function [Windows Shell], intsafe/UIntPtrToInt8, shell.UIntPtrToInt8
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	intsafe.h
api_name:
-	UIntPtrToInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToInt8 function


## -description


Converts a value of type <b>UINT_PTR</b> to a value of type <b>INT8</b>.


## -parameters




### -param uOperand [in]

The value to convert.


### -param pi8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



