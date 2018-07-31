---
UID: NF:winbase.GetCommConfig
title: GetCommConfig function
author: windows-sdk-content
description: Retrieves the current configuration of a communications device.
old-location: base\getcommconfig.htm
old-project: DevIO
ms.assetid: 8c5b74f7-54e3-42c1-a111-a8ddfb677d4e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCommConfig, GetCommConfig function, _win32_getcommconfig, base.getcommconfig, winbase/GetCommConfig
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
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommConfig
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCommConfig function


## -description


Retrieves the current configuration of a communications device.

To retrieve the default configuration settings from the device manager, use the <a href="https://msdn.microsoft.com/04bf5033-17c3-4403-8386-f3144e11423f">GetDefaultCommConfig</a> function.


## -parameters




### -param hCommDev [in]

A handle to the open communications device. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


### -param lpCC [out]

A pointer to a buffer that receives a 
<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a> structure.


### -param lpdwSize [in, out]

The size, in bytes, of the buffer pointed to by <i>lpCC</i>. When the function returns, the variable contains the number of bytes copied if the function succeeds, or the number of bytes required if the buffer was too small.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/04bf5033-17c3-4403-8386-f3144e11423f">GetDefaultCommConfig</a>



<a href="https://msdn.microsoft.com/e38be757-81c6-49ae-8d90-4387893e8ec5">SetCommConfig</a>
 

 

