---
UID: NF:intsafe.SSIZETMult
title: SSIZETMult function
author: windows-sdk-content
description: Multiplies one SSIZE_T value by another.
old-location: shell\SSIZETMult.htm
tech.root: shell
ms.assetid: 9b698951-dd9d-427c-9f95-63392ef0f0d4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SSIZETMult, SSIZETMult function [Windows Shell], intsafe/SSIZETMult, shell.SSIZETMult
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
 - SSIZETMult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SSIZETMult function


## -description


Multiplies one SSIZE_T value by another.


## -parameters




### -param Multiplicand [in]

The number to be multiplied.


### -param Multiplier [in]

The number by which to multiply <i>Multiplicand</i>.


### -param pResult [out]

When this function returns successfully, points to the product of <i>Multiplicand</i> times <i>Multiplier</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



