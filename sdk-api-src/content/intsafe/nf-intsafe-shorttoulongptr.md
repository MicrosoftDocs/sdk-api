---
UID: NF:intsafe.ShortToULongPtr
title: ShortToULongPtr function
author: windows-sdk-content
description: Converts a value of type SHORT to a value of type ULONG_PTR.
old-location: shell\ShortToULongPtr.htm
old-project: shell
ms.assetid: 92600b01-55da-4f71-bbfd-96df43c1b6a5
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ShortToULongPtr, ShortToULongPtr function [Windows Shell], intsafe/ShortToULongPtr, shell.ShortToULongPtr
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - ShortToULongPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ShortToULongPtr function


## -description


Converts a value of type <b>SHORT</b> to a value of type <b>ULONG_PTR</b>.


## -parameters




### -param sOperand [in]

The value to convert.


### -param pulResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



