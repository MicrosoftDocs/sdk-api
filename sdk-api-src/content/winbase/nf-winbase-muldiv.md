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

# MulDiv function


## -description


Multiplies two 32-bit values and then divides the 64-bit result by a third 32-bit value. The final result is rounded to the nearest integer.


## -parameters




### -param nNumber [in]

The multiplicand.


### -param nNumerator [in]

The multiplier.


### -param nDenominator [in]

The number by which the result of the multiplication operation is to be divided.


## -returns



If the function succeeds, the return value is the result of the multiplication and division, rounded to the nearest integer. If the result is a positive half integer (ends in .5), it is rounded up. If the result is a negative half integer, it is rounded down.

If either an overflow occurred or <i>nDenominator</i> was 0, the return value is -1.




## -see-also




<a href="https://msdn.microsoft.com/5c0caf42-2a2f-4eae-b0be-e8bb1b87dd9d">Int32x32To64</a>



<a href="https://msdn.microsoft.com/db4ffbd5-d9e4-4c95-83cc-6f0691c080d2">Large Integers</a>



<a href="https://msdn.microsoft.com/369e0574-df8b-4e65-bbba-7a7961caebe7">UInt32x32To64</a>
 

 

