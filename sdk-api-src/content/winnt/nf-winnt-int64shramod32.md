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

# Int64ShraMod32 macro


## -description


Performs a right arithmetic shift operation on a signed 64-bit integer value. The function provides improved shifting code for right arithmetic shifts where the shift count is in the range 0-31.


## -parameters




### -param a

TBD


### -param b

TBD






#### - ShiftCount [in]

The shift count in the range 0-31.


#### - Value [in]

The signed 64-bit integer to be shifted.


## -remarks



The shift count is the number of bit positions that the value's bits move.

In a right arithmetic shift operation on a signed value, the value's bits move to the right, and vacated bits on the left side of the value are set to the value of the sign bit.

A compiler can generate optimal code for a right arithmetic shift operation when the shift count is a constant. However, if the shift count is a variable whose range of values is unknown, the compiler must assume the worst case, leading to non-optimal code: code that calls a subroutine, or code that is inline but branches. By restricting the shift count to the range 0-31, the 
<b>Int64ShraMod32</b> function lets the compiler generate optimal or near-optimal code.

Please note that the 
<b>Int64ShraMod32</b> function's <i>Value</i> parameter and return value are 64-bit values, not 
<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/fe79b0c4-3316-4b05-b088-0d4b45586430">Int64ShllMod32</a>



<a href="https://msdn.microsoft.com/95ce281a-92b1-4c9b-a345-6b50f0285d65">Int64ShrlMod32</a>



<a href="https://msdn.microsoft.com/db4ffbd5-d9e4-4c95-83cc-6f0691c080d2">Large Integers</a>
 

 

