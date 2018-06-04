---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetCommState function


## -description


Configures a communications device according to the specifications in a device-control block (a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure). The function reinitializes all hardware and control settings, but it does not empty output or input queues.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function returns this handle.


### -param lpDCB [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure that contains the configuration information for the specified communications device.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SetCommState</b> function uses a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure to specify the desired configuration. The 
<a href="https://msdn.microsoft.com/974c2ddc-9f7f-445e-ac47-8cd86817ce9b">GetCommState</a> function returns the current configuration.

To set only a few members of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure, you should modify a 
<b>DCB</b> structure that has been filled in by a call to 
<a href="https://msdn.microsoft.com/974c2ddc-9f7f-445e-ac47-8cd86817ce9b">GetCommState</a>. This ensures that the other members of the 
<b>DCB</b> structure have appropriate values.

The 
<b>SetCommState</b> function fails if the <b>XonChar</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure is equal to the <b>XoffChar</b> member.

When 
<b>SetCommState</b> is used to configure the 8250, the following restrictions apply to the values for the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure's <b>ByteSize</b> and <b>StopBits</b> members:

The number of data bits must be 5 to 8 bits.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/5b325a1e-51e1-43b4-92e7-7bcf34c6388f">Configuring a Communications Resource</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6ecd497d-2247-4b6b-8751-c107717de434">BuildCommDCB</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a>



<a href="https://msdn.microsoft.com/974c2ddc-9f7f-445e-ac47-8cd86817ce9b">GetCommState</a>
 

 

