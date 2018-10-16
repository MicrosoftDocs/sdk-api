---
UID: NF:intsafe.LongMult
title: LongMult function
author: windows-sdk-content
description: Multiplies two values of type LONG.
old-location: shell\LongMult.htm
tech.root: shell
ms.assetid: 7eef49ae-98bf-486d-bdcf-1d573e66f5f5
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: LongMult, LongMult function [Windows Shell], intsafe/LongMult, shell.LongMult
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
 - LongMult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LongMult function


## -description


Multiplies two values of type <b>LONG</b>.


## -parameters




### -param lMultiplicand [in]

The first value.


### -param lMultiplier [in]

The second value.


### -param plResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



