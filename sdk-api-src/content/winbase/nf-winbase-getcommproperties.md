---
UID: NF:winbase.GetCommProperties
title: GetCommProperties function
author: windows-sdk-content
description: Retrieves information about the communications properties for a specified communications device.
old-location: base\getcommproperties.htm
old-project: devio
ms.assetid: dbbf55d6-d369-4b28-bdc7-1fd9a736e658
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetCommProperties, GetCommProperties function, _win32_getcommproperties, base.getcommproperties, winbase/GetCommProperties
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
 - GetCommProperties
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCommProperties function


## -description


Retrieves information about the communications properties for a specified communications device.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


### -param lpCommProp [out]

A pointer to a 
<a href="https://msdn.microsoft.com/d50ff606-1939-4e36-ba83-da8f269a3cc8">COMMPROP</a> structure in which the communications properties information is returned. This information can be used in subsequent calls to the 
<a href="https://msdn.microsoft.com/a9296514-4789-4830-ba68-84a16ac7fc47">SetCommState</a>, 
<a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a>, or 
<a href="https://msdn.microsoft.com/7b42fdad-5847-4036-957e-2f71ad982d9f">SetupComm</a> function to configure the communications device.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetCommProperties</b> function returns information from a device driver about the configuration settings that are supported by the driver.




## -see-also




<a href="https://msdn.microsoft.com/d50ff606-1939-4e36-ba83-da8f269a3cc8">COMMPROP</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/a9296514-4789-4830-ba68-84a16ac7fc47">SetCommState</a>



<a href="https://msdn.microsoft.com/71aa6ab3-d56c-43bc-9932-5b4e61fc4b30">SetCommTimeouts</a>



<a href="https://msdn.microsoft.com/7b42fdad-5847-4036-957e-2f71ad982d9f">SetupComm</a>
 

 

