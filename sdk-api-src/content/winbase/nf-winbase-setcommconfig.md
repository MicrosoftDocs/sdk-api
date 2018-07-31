---
UID: NF:winbase.SetCommConfig
title: SetCommConfig function
author: windows-sdk-content
description: Sets the current configuration of a communications device.
old-location: base\setcommconfig.htm
old-project: DevIO
ms.assetid: e38be757-81c6-49ae-8d90-4387893e8ec5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetCommConfig, SetCommConfig function, _win32_setcommconfig, base.setcommconfig, winbase/SetCommConfig
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
 - SetCommConfig
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetCommConfig function


## -description


Sets the current configuration of a communications device.


## -parameters




### -param hCommDev [in]

A handle to the open communications device. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


### -param lpCC [in]

A pointer to a 
<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a> structure.


### -param dwSize [in]

The size of the structure pointed to by <i>lpCC</i>, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/8c5b74f7-54e3-42c1-a111-a8ddfb677d4e">GetCommConfig</a>
 

 

