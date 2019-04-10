---
UID: NS:ddrawint._DD_HALINFO
title: DD_HALINFO (ddrawint.h)
author: windows-sdk-content
description: The DD_HALINFO structure describes the capabilities of the hardware and driver.
old-location: display\dd_halinfo.htm
tech.root: display
ms.assetid: 99ecd219-1e85-4904-867d-3efcb378bb11
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDD_HALINFO, DD_HALINFO, DD_HALINFO structure [Display Devices], PDD_HALINFO, PDD_HALINFO structure pointer [Display Devices], ddrawint/DD_HALINFO, ddrawint/PDD_HALINFO, ddstrcts_3b4465cc-0f18-431c-b0a5-bf5bfb854f05.xml, display.dd_halinfo"
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_HALINFO
product: Windows
targetos: Windows
req.typenames: DD_HALINFO, *PDD_HALINFO
req.redist: 
---

# DD_HALINFO structure


## -description


The DD_HALINFO structure describes the capabilities of the hardware and driver.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_HALINFO structure.


### -field vmiData

Specifies a <a href="https://msdn.microsoft.com/c5df8f26-3eb1-4743-96d1-7b73d902be8d">VIDEOMEMORYINFO</a> structure that describes the display's memory.


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

Points to a <a href="https://msdn.microsoft.com/4aba7417-8391-4ae7-a449-dbc307cab530">D3DHAL_GLOBALDRIVERDATA</a> structure that describes the 3D capabilities of the driver and its device. 


### -field lpD3DHALCallbacks

Points to the driver's initialized <a href="https://msdn.microsoft.com/3b045732-a41f-47e7-9835-41e3ef54f14c">D3DHAL_CALLBACKS</a> structure.


### -field lpD3DBufCallbacks

Used only by drivers that want to implement driver level vertex and command buffer allocation. This is usually done for performance reasons. The <b>lpD3DBufCallbacks</b> member is a pointer to a <a href="https://msdn.microsoft.com/59fa4043-6238-49f7-b9d6-58c1f215865a">DD_D3DBUFCALLBACKS</a> structure that the driver fills out with the callbacks used to support driver managed vertex and command buffers. This member should normally be ignored by the driver. 


## -remarks



GDI allocates and zero-initializes the DD_HALINFO structure and passes it to the driver's <a href="https://msdn.microsoft.com/c6068572-bd73-4faa-b085-9608ebc450ea">DrvGetDirectDrawInfo</a> routine to be initialized with driver-specific data.




## -see-also




<a href="https://msdn.microsoft.com/3b045732-a41f-47e7-9835-41e3ef54f14c">D3DHAL_CALLBACKS</a>



<a href="https://msdn.microsoft.com/4aba7417-8391-4ae7-a449-dbc307cab530">D3DHAL_GLOBALDRIVERDATA</a>



<a href="https://msdn.microsoft.com/529d60b5-658d-4d55-a599-fa35386c01a7">DDCORECAPS</a>



<a href="https://msdn.microsoft.com/59fa4043-6238-49f7-b9d6-58c1f215865a">DD_D3DBUFCALLBACKS</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>



<a href="https://msdn.microsoft.com/c6068572-bd73-4faa-b085-9608ebc450ea">DrvGetDirectDrawInfo</a>



<a href="https://msdn.microsoft.com/c5df8f26-3eb1-4743-96d1-7b73d902be8d">VIDEOMEMORYINFO</a>
 

 

