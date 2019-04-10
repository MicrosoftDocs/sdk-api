---
UID: NS:ddrawint._DD_COLORCONTROLDATA
title: DD_COLORCONTROLDATA (ddrawint.h)
author: windows-sdk-content
description: The DD_COLORCONTROLDATA structure contains the color control information for the specified overlay.
old-location: display\dd_colorcontroldata.htm
tech.root: display
ms.assetid: 7c983faa-de9d-4a04-ac8d-d37fb182a662
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDD_COLORCONTROLDATA, DD_COLORCONTROLDATA, DD_COLORCONTROLDATA structure [Display Devices], ddrawint/DD_COLORCONTROLDATA, ddstrcts_5bc6386d-437a-4fa7-b9ac-def03150b340.xml, display.dd_colorcontroldata"
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
 - DD_COLORCONTROLDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_COLORCONTROLDATA, DD_COLORCONTROLDATA"
req.redist: 
---

# DD_COLORCONTROLDATA structure


## -description


The DD_COLORCONTROLDATA structure contains the color control information for the specified overlay.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSurface

Points to the <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure representing the overlay surface.


### -field lpColorData

Points to a <a href="https://msdn.microsoft.com/77c19de1-a046-4752-b9af-a9865861a493">DDCOLORCONTROL</a> structure. See the <b>dwFlags</b> member to determine how to use this member.


### -field dwFlags

Indicates a set of flags that specify the color control flags. This member can be one of the following values: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDRAWI_GETCOLOR

</td>
<td>
The driver should return the color controls it supports for the specified overlay in the <b>lpColorData</b> member. The driver should set the appropriate flags in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/77c19de1-a046-4752-b9af-a9865861a493">DDCOLORCONTROL</a> structure to indicate in which other members the driver has returned valid data.

</td>
</tr>
<tr>
<td>
DDRAWI_SETCOLOR

</td>
<td>
The driver should set the current color controls for the specified overlay using the values specified in the <b>lpColorData</b> member.

</td>
</tr>
</table>
 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/626fdd37-bebb-47b7-9899-7cf0dc2bd1ba">DdControlColor</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field ColorControl

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/626fdd37-bebb-47b7-9899-7cf0dc2bd1ba">DdControlColor</a>
 

 

