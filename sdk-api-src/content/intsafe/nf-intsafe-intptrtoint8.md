---
UID: NF:intsafe.IntPtrToInt8
title: IntPtrToInt8 function
author: windows-sdk-content
description: Converts a value of type INT_PTR to a value of type INT8.
old-location: shell\IntPtrToInt8.htm
old-project: shell
ms.assetid: b453eb77-fcf4-4f0b-8662-88e91f73c7b7
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IntPtrToInt8, IntPtrToInt8 function [Windows Shell], intsafe/IntPtrToInt8, shell.IntPtrToInt8
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
-	IntPtrToInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntPtrToInt8 function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>INT8</b>.


## -parameters




### -param iOperand [in]

The value to convert.


### -param pi8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



