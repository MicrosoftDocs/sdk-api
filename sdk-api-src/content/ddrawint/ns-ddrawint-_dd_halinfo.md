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

# _DD_HALINFO structure


## -description


The DD_HALINFO structure describes the capabilities of the hardware and driver.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_HALINFO structure.


### -field vmiData

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570172">VIDEOMEMORYINFO</a> structure that describes the display's memory.


### -field ddCaps

Specifies a <b>DDNTCORECAPS</b> structure that contains driver-specific capabilities.


### -field GetDriverInfo

Points to the driver's <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function. This function is called to get further Microsoft DirectDraw driver information. This member can be <b>NULL</b>.


### -field dwFlags

Specifies the display driver's creation flags. This member is a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDHALINFO_ISPRIMARYDISPLAY

</td>
<td>
The driver is the primary display driver.

</td>
</tr>
<tr>
<td>
DDHALINFO_MODEXILLEGAL

</td>
<td>
This hardware does not support ModeX modes.

</td>
</tr>
<tr>
<td>
DDHALINFO_GETDRIVERINFOSET

</td>
<td>
The <b>GetDriverInfo</b> member is set.

</td>
</tr>
<tr>
<td>
DDHALINFO_GETDRIVERINFO2

</td>
<td>
Driver supports <b>GetDriverInfo2</b> variant of <b>GetDriverInfo</b>.

</td>
</tr>
</table>
 


### -field lpD3DGlobalDriverData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545963">D3DHAL_GLOBALDRIVERDATA</a> structure that describes the 3D capabilities of the driver and its device. 


### -field lpD3DHALCallbacks

Points to the driver's initialized <a href="https://msdn.microsoft.com/library/windows/hardware/ff544716">D3DHAL_CALLBACKS</a> structure.


### -field lpD3DBufCallbacks

Used only by drivers that want to implement driver level vertex and command buffer allocation. This is usually done for performance reasons. The <b>lpD3DBufCallbacks</b> member is a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550557">DD_D3DBUFCALLBACKS</a> structure that the driver fills out with the callbacks used to support driver managed vertex and command buffers. This member should normally be ignored by the driver. 


## -remarks



GDI allocates and zero-initializes the DD_HALINFO structure and passes it to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a> routine to be initialized with driver-specific data.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544716">D3DHAL_CALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545963">D3DHAL_GLOBALDRIVERDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550557">DD_D3DBUFCALLBACKS</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570172">VIDEOMEMORYINFO</a>
 

 

