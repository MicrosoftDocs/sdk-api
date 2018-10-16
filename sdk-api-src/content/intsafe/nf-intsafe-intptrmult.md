---
UID: NF:intsafe.IntPtrMult
title: IntPtrMult function
author: windows-sdk-content
description: Multiplies two values of type INT_PTR.
old-location: shell\IntPtrMult.htm
tech.root: shell
ms.assetid: c93c088e-bef2-4999-bd6d-68d4dd493f0b
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IntPtrMult, IntPtrMult function [Windows Shell], intsafe/IntPtrMult, shell.IntPtrMult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - IntPtrMult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntPtrMult function


## -description


Multiplies two values of type <b>INT_PTR</b>.


## -parameters




### -param iMultiplicand [in]

The first value.


### -param iMultiplier [in]

The second value.


### -param piResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



