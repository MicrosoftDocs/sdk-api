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

# _DD_VPORTCOLORDATA structure


## -description


The DD_VPORTCOLORDATA structure contains the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object color control information.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.


### -field dwFlags

Specifies the color control operation to be performed by the driver. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDRAWI_VPORTGETCOLOR

</td>
<td>
The driver should write the current VPE object color controls into the DDCOLORCONTROL structure to which <b>lpColorData</b> points.

</td>
</tr>
<tr>
<td>
DDRAWI_VPORTSETCOLOR

</td>
<td>
The driver should set new values for the VPE object color controls based on the contents of the DDCOLORCONTROL structure to which <b>lpColorData</b> points.

</td>
</tr>
</table>
 


### -field lpColorData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549237">DDCOLORCONTROL</a> structure that defines the color control associated with the VPE object to which <b>lpVideoPort</b> points. The value of <b>dwFlags</b> determines whether the driver reads from or writes to this structure.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/0d4d5157-cadf-4b63-aafc-ccb252cec2b4">DdVideoPortColorControl</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field ColorControl

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549237">DDCOLORCONTROL</a>



<a href="https://msdn.microsoft.com/0d4d5157-cadf-4b63-aafc-ccb252cec2b4">DdVideoPortColorControl</a>
 

 

