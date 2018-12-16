---
UID: NF:winnt.Int32x32To64
title: Int32x32To64 macro
author: windows-sdk-content
description: Multiplies two signed 32-bit integers, returning a signed 64-bit integer result.
old-location: winprog\int32x32to64.htm
tech.root: WinProg
ms.assetid: 5c0caf42-2a2f-4eae-b0be-e8bb1b87dd9d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Int32x32To64, Int32x32To64 macro [Windows API], _win32_int32x32to64, winnt/Int32x32To64, winprog.int32x32to64
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - Int32x32To64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Int32x32To64 macro


## -description


Multiplies two signed 32-bit integers, returning a signed 64-bit integer result. The function performs optimally on 32-bit Windows.


## -parameters




### -param a [in]

The first signed 32-bit integer for the multiplication operation.


### -param b [in]

The second signed 32-bit integer for the multiplication operation.


## -remarks



This function is implemented on all platforms by optimal inline code: a single multiply instruction that returns a 64-bit result.

Please note that the function's return value is a 64-bit value, not a 
<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/db4ffbd5-d9e4-4c95-83cc-6f0691c080d2">Large Integers</a>



<a href="https://msdn.microsoft.com/369e0574-df8b-4e65-bbba-7a7961caebe7">UInt32x32To64</a>
 

 

