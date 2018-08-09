---
UID: NF:winbase.MulDiv
title: MulDiv function
author: windows-sdk-content
description: Multiplies two 32-bit values and then divides the 64-bit result by a third 32-bit value.
old-location: winprog\muldiv.htm
old-project: winprog
ms.assetid: 30419ce3-3874-4066-91c8-7f63dfb50169
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MulDiv, MulDiv function [Windows API], _win32_muldiv, winbase/MulDiv, winprog.muldiv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-LargeInteger-L1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - MulDiv
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

