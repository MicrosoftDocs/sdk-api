---
UID: NF:winnt.UInt32x32To64
title: UInt32x32To64 macro
author: windows-driver-content
description: Multiplies two unsigned 32-bit integers, returning an unsigned 64-bit integer result.
old-location: winprog\uint32x32to64.htm
old-project: WinProg
ms.assetid: 369e0574-df8b-4e65-bbba-7a7961caebe7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: UInt32x32To64, UInt32x32To64 macro [Windows API], _win32_uint32x32to64, winnt/UInt32x32To64, winprog.uint32x32to64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	UInt32x32To64
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UInt32x32To64 macro


## -description


Multiplies two unsigned 32-bit integers, returning an unsigned 64-bit integer result. The function performs optimally on 32-bit Windows.


## -parameters




### -param a

TBD


### -param b

TBD






#### - Multiplicand [in]

The second unsigned 32-bit integer for the multiplication operation.


#### - Multiplier [in]

The first unsigned 32-bit integer for the multiplication operation.


## -remarks



This function is implemented on all platforms by optimal inline code: a single multiply instruction that returns a 64-bit result.

Please note that the function's return value is a 64-bit value, not a 
<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/5c0caf42-2a2f-4eae-b0be-e8bb1b87dd9d">Int32x32To64</a>



<a href="https://msdn.microsoft.com/db4ffbd5-d9e4-4c95-83cc-6f0691c080d2">Large Integers</a>
 

 

