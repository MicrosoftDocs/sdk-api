---
UID: NF:winbase.SetCommState
title: SetCommState function
author: windows-sdk-content
description: Configures a communications device according to the specifications in a device-control block (a DCB structure). The function reinitializes all hardware and control settings, but it does not empty output or input queues.
old-location: base\setcommstate.htm
tech.root: devio
ms.assetid: a9296514-4789-4830-ba68-84a16ac7fc47
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: SetCommState, SetCommState function, _win32_setcommstate, base.setcommstate, winbase/SetCommState
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
 - SetCommState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetCommState function


## -description


Configures a communications device according to the specifications in a device-control block (a 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure). The function reinitializes all hardware and control settings, but it does not empty output or input queues.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


### -param lpDCB [in]

A pointer to a 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure that contains the configuration information for the specified communications device.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SetCommState</b> function uses a 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure to specify the desired configuration. The 
<a href="https://msdn.microsoft.com/974c2ddc-9f7f-445e-ac47-8cd86817ce9b">GetCommState</a> function returns the current configuration.

To set only a few members of the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure, you should modify a 
<b>DCB</b> structure that has been filled in by a call to 
<a href="https://msdn.microsoft.com/974c2ddc-9f7f-445e-ac47-8cd86817ce9b">GetCommState</a>. This ensures that the other members of the 
<b>DCB</b> structure have appropriate values.

The 
<b>SetCommState</b> function fails if the <b>XonChar</b> member of the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure is equal to the <b>XoffChar</b> member.

When 
<b>SetCommState</b> is used to configure the 8250, the following restrictions apply to the values for the 
<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a> structure's <b>ByteSize</b> and <b>StopBits</b> members:

The number of data bits must be 5 to 8 bits.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/5b325a1e-51e1-43b4-92e7-7bcf34c6388f">Configuring a Communications Resource</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6ecd497d-2247-4b6b-8751-c107717de434">BuildCommDCB</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/9dccd2c6-44b7-4609-a2b9-9815430bf3c7">DCB</a>



<a href="https://msdn.microsoft.com/974c2ddc-9f7f-445e-ac47-8cd86817ce9b">GetCommState</a>
 

 

