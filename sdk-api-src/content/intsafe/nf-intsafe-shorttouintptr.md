---
UID: NF:intsafe.ShortToUIntPtr
title: ShortToUIntPtr function
author: windows-sdk-content
description: Converts a value of type SHORT to a value of type UINT_PTR.
old-location: shell\ShortToUIntPtr.htm
old-project: shell
ms.assetid: 6b5d0c0c-a2c3-4d63-ab6c-d93372a7413e
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: ShortToUIntPtr, ShortToUIntPtr function [Windows Shell], intsafe/ShortToUIntPtr, shell.ShortToUIntPtr
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
 - ShortToUIntPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ShortToUIntPtr function


## -description


Converts a value of type <b>SHORT</b> to a value of type <b>UINT_PTR</b>.


## -parameters




### -param sOperand [in]

The value to convert.


### -param puResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



