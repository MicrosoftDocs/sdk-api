---
UID: NF:winnt.Int64ShraMod32
title: Int64ShraMod32 macro
author: windows-sdk-content
description: Performs a right arithmetic shift operation on a signed 64-bit integer value. The function provides improved shifting code for right arithmetic shifts where the shift count is in the range 0-31.
old-location: winprog\int64shramod32.htm
old-project: WinProg
ms.assetid: 69de2eb7-2cbe-48db-935b-b3d2c41f4e86
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: Int64ShraMod32, Int64ShraMod32 macro [Windows API], _win32_int64shramod32, winnt/Int64ShraMod32, winprog.int64shramod32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	Int64ShraMod32
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

