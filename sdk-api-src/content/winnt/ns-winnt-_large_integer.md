---
UID: NS:winnt._LARGE_INTEGER
title: "_LARGE_INTEGER"
author: windows-sdk-content
description: Represents a 64-bit signed integer value.
old-location: winprog\large_integer_str.htm
tech.root: WinProg
ms.assetid: 6a2985b6-5baf-49ab-af28-67c1374557ea
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PLARGE_INTEGER, LARGE_INTEGER, LARGE_INTEGER union [Windows API], PLARGE_INTEGER, PLARGE_INTEGER union pointer [Windows API], _LARGE_INTEGER, _win32_large_integer_str, winnt/LARGE_INTEGER, winnt/PLARGE_INTEGER, winprog.large_integer_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - LARGE_INTEGER
product: Windows
targetos: Windows
req.typenames: LARGE_INTEGER
req.redist: 
---

# _LARGE_INTEGER structure


## -description


Represents a 64-bit signed integer value.
<div class="alert"><b>Note</b>  Your C compiler may support 64-bit integers natively. For example, Microsoft Visual C++ supports the <a href="https://msdn.microsoft.com/52fafae2-003c-4eae-b6e1-a49f69db204e">__int64</a> sized integer type. For more information, see the documentation included with your C compiler.</div><div> </div>

## -struct-fields




### -field QuadPart

A signed 64-bit integer.


#### - HighPart

The high-order 32 bits.


#### - LowPart

The low-order 32 bits.


#### - u



#### LowPart

The low-order 32 bits.



#### HighPart

The high-order 32 bits.


## -remarks



The 
<b>LARGE_INTEGER</b> structure is actually a union. If your compiler has built-in support for 64-bit integers, use the <b>QuadPart</b> member to store the 64-bit integer. Otherwise, use the <b>LowPart</b> and <b>HighPart</b> members to store the 64-bit integer.




## -see-also




<a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>
 

 

