---
UID: NS:winnt._ULARGE_INTEGER
title: "_ULARGE_INTEGER"
author: windows-sdk-content
description: Represents a 64-bit unsigned integer value.
old-location: winprog\ularge_integer_str.htm
old-project: WinProg
ms.assetid: 83a10c12-2cd1-449a-af3f-b2138fc50ee0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PULARGE_INTEGER, PULARGE_INTEGER, PULARGE_INTEGER union pointer [Windows API], ULARGE_INTEGER, ULARGE_INTEGER union [Windows API], _ULARGE_INTEGER, _win32_ularge_integer_str, winnt/PULARGE_INTEGER, winnt/ULARGE_INTEGER, winprog.ularge_integer_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: ULARGE_INTEGER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ULARGE_INTEGER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ULARGE_INTEGER structure


## -description


Represents a 64-bit unsigned integer value.
<div class="alert"><b>Note</b>  Your C compiler may support 64-bit integers natively. For example, Microsoft Visual C++ supports the <a href="https://msdn.microsoft.com/">__int64</a> sized integer type. For more information, see the documentation included with your C compiler.</div><div> </div>

## -struct-fields




### -field QuadPart

An unsigned 64-bit integer.


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
<b>ULARGE_INTEGER</b> structure is actually a union. If your compiler has built-in support for 64-bit integers, use the <b>QuadPart</b> member to store the 64-bit integer. Otherwise, use the <b>LowPart</b> and <b>HighPart</b> members to store the 64-bit integer.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
 

 

