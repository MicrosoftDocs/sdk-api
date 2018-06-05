---
UID: NF:winbase.SetDefaultCommConfigW
title: SetDefaultCommConfigW function
author: windows-sdk-content
description: Sets the default configuration for a communications device.
old-location: base\setdefaultcommconfig.htm
old-project: DevIO
ms.assetid: 3b228b56-34ca-4b37-af67-4e4e1fa60df2
ms.author: windowssdkdev
ms.date: 04/03/2018
ms.keywords: SetDefaultCommConfig, SetDefaultCommConfig function, SetDefaultCommConfigA, SetDefaultCommConfigW, _win32_setdefaultcommconfig, base.setdefaultcommconfig, winbase/SetDefaultCommConfig, winbase/SetDefaultCommConfigA, winbase/SetDefaultCommConfigW
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
req.unicode-ansi: SetDefaultCommConfigW (Unicode) and SetDefaultCommConfigA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
api_name:
-	SetDefaultCommConfig
-	SetDefaultCommConfigA
-	SetDefaultCommConfigW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetDefaultCommConfigW function


## -description


Sets the default configuration for a communications device.


## -parameters




### -param lpszName [in]

The name of the device. For example, COM1 through COM9 are serial ports and LPT1 through LPT9 are parallel ports.


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



<a href="https://msdn.microsoft.com/04bf5033-17c3-4403-8386-f3144e11423f">GetDefaultCommConfig</a>
 

 

