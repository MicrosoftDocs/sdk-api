---
UID: NF:winbase.GetDefaultCommConfigA
title: GetDefaultCommConfigA function
author: windows-sdk-content
description: Retrieves the default configuration for the specified communications device.
old-location: base\getdefaultcommconfig.htm
old-project: DevIO
ms.assetid: 04bf5033-17c3-4403-8386-f3144e11423f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetDefaultCommConfig, GetDefaultCommConfig function, GetDefaultCommConfigA, GetDefaultCommConfigW, _win32_getdefaultcommconfig, base.getdefaultcommconfig, winbase/GetDefaultCommConfig, winbase/GetDefaultCommConfigA, winbase/GetDefaultCommConfigW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetDefaultCommConfigW (Unicode) and GetDefaultCommConfigA (ANSI)
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
api_name:
 - GetDefaultCommConfig
 - GetDefaultCommConfigA
 - GetDefaultCommConfigW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetDefaultCommConfigA function


## -description


Retrieves the default configuration for the specified communications device.


## -parameters




### -param lpszName [in]

The name of the device. For example, COM1 through COM9 are serial ports and LPT1 through LPT9 are parallel ports.


### -param lpCC [out]

A pointer to a buffer that receives a 
<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a> structure.


### -param lpdwSize [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by <i>lpCC</i>, in bytes. Upon return, the variable contains the number of bytes copied if the function succeeds, or the number of bytes required if the buffer was too small.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/3b228b56-34ca-4b37-af67-4e4e1fa60df2">SetDefaultCommConfig</a>
 

 

