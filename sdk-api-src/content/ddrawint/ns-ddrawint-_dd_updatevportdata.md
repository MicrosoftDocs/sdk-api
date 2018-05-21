---
UID: NS:ddrawint._DD_UPDATEVPORTDATA
title: "_DD_UPDATEVPORTDATA"
author: windows-driver-content
description: The DD_UPDATEVPORTDATA structure contains the information required to start, stop, and change the video port extensions (VPE) object.
old-location: display\dd_updatevportdata.htm
old-project: display
ms.assetid: e1ba7851-570e-4ddc-8981-766294011409
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PDD_UPDATEVPORTDATA, DD_UPDATEVPORTDATA, DD_UPDATEVPORTDATA structure [Display Devices], _DD_UPDATEVPORTDATA, ddrawint/DD_UPDATEVPORTDATA, ddstrcts_a266490e-9cac-45ca-9129-63f3dcef6a6f.xml, display.dd_updatevportdata"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: "*PDD_UPDATEVPORTDATA, DD_UPDATEVPORTDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_UPDATEVPORTDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_UPDATEVPORTDATA structure


## -description


The DD_UPDATEVPORTDATA structure contains the information required to start, stop, and change the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.


### -field lplpDDSurface

Points to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff551730">DD_SURFACE_INT</a> structures that represent regular video surfaces. This member can be <b>NULL</b>.


### -field lplpDDVBISurface

Points to an array of DD_SURFACE_INT structures that represent <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> surfaces. This member can be <b>NULL</b>.


### -field lpVideoInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550447">DDVIDEOPORTINFO</a> structure that describes how the VPE object should transfer video data to a surface. This member can be <b>NULL</b> when <b>dwFlags</b> is DDRAWI_VPORTSTOP.


### -field dwFlags

Indicates the action to be performed by the VPE object. This member must be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDRAWI_VPORTSTART

</td>
<td>
The driver should start the flow of data through the VPE object.

</td>
</tr>
<tr>
<td>
DDRAWI_VPORTSTOP

</td>
<td>
The driver should stop the flow of data through the VPE object.

</td>
</tr>
<tr>
<td>
DDRAWI_VPORTUPDATE

</td>
<td>
<b>DdVideoPortUpdate</b> has been called with a new set of flags in the <b>dwVPFlags</b> member of the DDVIDEOPORTINFO structure to which <b>lpVideoInfo</b> points. The driver should change the flow of data through the VPE object according to the new flags.

</td>
</tr>
</table>
 


### -field dwNumAutoflip

Specifies the number of surfaces in the list to which <b>lplpDDSurface</b> points. If this member is greater than 1, <b>lplpDDSurface</b> is an array of surface structures to accommodate autoflipping.


### -field dwNumVBIAutoflip

Specifies the number of surfaces in the list to which <b>lplpDDVBISurface</b> points. If this member is greater than 1, <b>lplpDDVBISurface</b> is an array of surface structures to accommodate autoflipping of <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> data.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/50a55a89-bae0-4a65-96ef-3e9903f45a0c">DdVideoPortUpdate</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field UpdateVideoPort

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550447">DDVIDEOPORTINFO</a>



<a href="https://msdn.microsoft.com/50a55a89-bae0-4a65-96ef-3e9903f45a0c">DdVideoPortUpdate</a>
 

 

