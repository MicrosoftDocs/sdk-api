---
UID: NF:intsafe.IntPtrToLongPtr
title: IntPtrToLongPtr function
author: windows-sdk-content
description: Converts a value of type INT_PTR to a value of type LONG_PTR.
old-location: shell\IntPtrToLongPtr.htm
old-project: shell
ms.assetid: f0e4d121-9cc5-4fc9-a507-b9fc8e314f94
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IntPtrToLongPtr, IntPtrToLongPtr function [Windows Shell], intsafe/IntPtrToLongPtr, shell.IntPtrToLongPtr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - IntPtrToLongPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IntPtrToLongPtr function


## -description


Converts a value of type <b>INT_PTR</b> to a value of type <b>LONG_PTR</b>.


## -parameters




### -param iOperand [in]

The value to convert.


### -param plResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



