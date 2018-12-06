---
UID: NS:ddkmapi._DDGETSURFACESTATEOUT
title: "_DDGETSURFACESTATEOUT"
author: windows-sdk-content
description: The DDGETSURFACESTATEOUT structure contains the capabilities and status of the specified surface.
old-location: display\ddgetsurfacestateout.htm
tech.root: display
ms.assetid: 8d84fcdf-c880-4a3e-a57d-12bb8e59cb5b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDDGETSURFACESTATEOUT, DDGETSURFACESTATEOUT, DDGETSURFACESTATEOUT structure [Display Devices], LPDDGETSURFACESTATEOUT, LPDDGETSURFACESTATEOUT structure pointer [Display Devices], _DDGETSURFACESTATEOUT, ddkmapi/DDGETSURFACESTATEOUT, ddkmapi/LPDDGETSURFACESTATEOUT, ddstrcts_bfeeac46-f803-48ee-aac4-39cb4781f925.xml, display.ddgetsurfacestateout"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
 - ddkmapi.h
api_name:
 - DDGETSURFACESTATEOUT
product: Windows
targetos: Windows
req.typenames: DDGETSURFACESTATEOUT, *LPDDGETSURFACESTATEOUT
req.redist: 
---

# _DDGETSURFACESTATEOUT structure


## -description


The DDGETSURFACESTATEOUT structure contains the capabilities and status of the specified surface. 


## -struct-fields




### -field ddRVal

Specifies the location in which Microsoft DirectDraw writes the return value of the <a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a> function for <a href="https://msdn.microsoft.com/fa9710af-a66e-4ba9-ad0b-f79196e5b13e">DD_DXAPI_GET_SURFACE_STATE</a> operations. A return code of DD_OK indicates success.


### -field dwStateCaps

Contains the DirectDrawSurface's capabilities of the device. One or more of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSTATE_BOB

</td>
<td>
The device is capable of performing bob mode.

</td>
</tr>
<tr>
<td>
DDSTATE_WEAVE

</td>
<td>
The device is capable of performing weave mode.

</td>
</tr>
</table>
 


### -field dwStateStatus

Contains the status of the selected DirectDrawSurface. One or more of the following:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSTATE_BOB

</td>
<td>
Bob mode is being used on this surface.

</td>
</tr>
<tr>
<td>
DDSTATE_EXPLICITLY_SET

</td>
<td>
This state is due to a previous <a href="https://msdn.microsoft.com/8a792eee-d410-46c7-827e-62ad3360fead">DD_DXAPI_SET_SURFACE_STATE</a> call.

</td>
</tr>
<tr>
<td>
DDSTATE_SKIPEVENFIELDS

</td>
<td>
Stop bob or weave mode and skip every other field instead.

</td>
</tr>
<tr>
<td>
DDSTATE_SOFTWARE_AUTOFLIP

</td>
<td>
Software (as opposed to hardware) autoflipping is being used.

</td>
</tr>
<tr>
<td>
DDSTATE_WEAVE

</td>
<td>
Weave mode is being used on this surface.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/fa9710af-a66e-4ba9-ad0b-f79196e5b13e">DD_DXAPI_GET_SURFACE_STATE</a>



<a href="https://msdn.microsoft.com/c4b38376-b54f-4fbb-b305-5951a1ea76a1">DxApi</a>
 

 

