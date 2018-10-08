---
UID: NF:winbase.TransmitCommChar
title: TransmitCommChar function
author: windows-sdk-content
description: Transmits a specified character ahead of any pending data in the output buffer of the specified communications device.
old-location: base\transmitcommchar.htm
tech.root: devio
ms.assetid: 599c3d04-6cd3-41ac-88a8-752f4b83d46b
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: TransmitCommChar, TransmitCommChar function, _win32_transmitcommchar, base.transmitcommchar, winbase/TransmitCommChar
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
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
 - TransmitCommChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TransmitCommChar function


## -description


Transmits a specified character ahead of any pending data in the output buffer of the specified communications device.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function returns this handle.


### -param cChar [in]

The character to be transmitted.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>TransmitCommChar</b> function is useful for sending an interrupt character (such as a CTRL+C) to a host system.

If the device is not transmitting, 
<b>TransmitCommChar</b> cannot be called repeatedly. Once 
<b>TransmitCommChar</b> places a character in the output buffer, the character must be transmitted before the function can be called again. If the previous character has not yet been sent, 
<b>TransmitCommChar</b> returns an error.




## -see-also




<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a>



<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a>
 

 

