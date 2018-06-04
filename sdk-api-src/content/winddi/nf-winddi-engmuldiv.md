---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EngMulDiv function


## -description


The <b>EngMulDiv</b> function multiplies two 32-bit values and then divides the 64-bit result by a third 32-bit value. 


## -parameters




### -param a [in]

Specifies the 32-bit signed multiplicand.


### -param b [in]

Specifies the 32-bit signed multiplier.


### -param c [in]

Specifies the 32-bit signed divisor by which the result of <i>a</i>*<i>b</i> is to be divided.


## -returns



<b>EngMulDiv</b> returns the signed 32-bit result of the multiplication and division. The return value is rounded up or down to the nearest integer.




## -remarks



Drivers should not pass a zero divisor to <b>EngMulDiv</b>.



