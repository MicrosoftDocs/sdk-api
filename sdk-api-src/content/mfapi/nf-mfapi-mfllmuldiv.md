---
UID: NF:mfapi.MFllMulDiv
title: MFllMulDiv function
author: windows-sdk-content
description: Calculates ((a * b) + d) / c, where each term is a 64-bit signed value.
old-location: mf\mfllmuldiv.htm
tech.root: medfound
ms.assetid: ee369c2e-99a1-4ee4-ac67-02f14e11e269
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFllMulDiv, MFllMulDiv function [Media Foundation], mf.mfllmuldiv, mfapi/MFllMulDiv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFllMulDiv
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFllMulDiv function


## -description


Calculates ((a * b) + d) / c, where each term is a 64-bit signed value.


## -parameters




### -param a

A multiplier.


### -param b

Another multiplier.


### -param c

The divisor.


### -param d

The rounding factor.


## -returns



Returns the result of the calculation. If numeric overflow occurs, the function returns _I64_MAX (positive overflow) or LLONG_MIN (negative overflow). If Mfplat.dll cannot be loaded, the function returns _I64_MAX.




## -remarks



<div class="alert"><b>Note</b>  A previous version of this topic described the parameters incorrectly. The divisor is <i>c</i> and the rounding factor is <i>d</i>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

