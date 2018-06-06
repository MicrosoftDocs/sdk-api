---
UID: NF:intsafe.SSIZETSub
title: SSIZETSub function
author: windows-sdk-content
description: Subtracts one SSIZE_T value from another.
old-location: shell\SSIZETSub.htm
old-project: shell
ms.assetid: 8c7ca2cb-3753-4d65-9179-5c8e1782c7ff
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SSIZETSub, SSIZETSub function [Windows Shell], intsafe/SSIZETSub, shell.SSIZETSub
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
 - SSIZETSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# SSIZETSub function


## -description


Subtracts one SSIZE_T value from another.


## -parameters




### -param Minuend [in]

The value from which <i>Subtrahend</i> will be subtracted.


### -param Subtrahend [in]

The value to subtract from <i>Minuend</i>.


### -param pResult [out]

When this function returns successfully, points to the difference between <i>Minuend</i> and <i>Subtrahend</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



