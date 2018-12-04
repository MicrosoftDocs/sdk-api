---
UID: NC:ddrawint.PDD_VPORTCB_GETOUTPUTFORMATS
title: PDD_VPORTCB_GETOUTPUTFORMATS
author: windows-sdk-content
description: The DdVideoPortGetOutputFormats callback function determines the output formats that the VPE object supports.
old-location: display\ddvideoportgetoutputformats.htm
tech.root: display
ms.assetid: 8e9df88b-a50a-4838-9732-9f818936cbcb
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: DdVideoPortGetOutputFormats, DdVideoPortGetOutputFormats callback function [Display Devices], PDD_VPORTCB_GETOUTPUTFORMATS, PDD_VPORTCB_GETOUTPUTFORMATS callback, ddfncs_24c5f4e8-c9ee-4104-80e5-7f6ef21a1f22.xml, ddrawint/DdVideoPortGetOutputFormats, display.ddvideoportgetoutputformats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortGetOutputFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_VPORTCB_GETOUTPUTFORMATS callback function


## -description


The <b>DdVideoPortGetOutputFormats</b> callback function determines the output formats that the VPE object supports.


## -parameters




### -param Arg1








#### - lpGetOutputFormats

Points to a <a href="https://msdn.microsoft.com/3033a4e9-3f94-4702-9db8-098a358ab1c2">DD_GETVPORTOUTPUTFORMATDATA</a> structure that contains the information required for the driver to return the output formats the VPE object supports.


## -returns



<b>DdVideoPortGetOutputFormats</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support VPE must implement <b>DdVideoPortGetOutputFormats</b>

DirectDraw calls <b>DdVideoPortGetOutputFormats</b> to obtain the number of output formats supported by the specified VPE object and a description of each format. <b>DdVideoPortGetOutputFormats</b> is called twice for the specified VPE object:

<ul>
<li>
In the first call, the <b>lpddpfOutputFormats</b> member of the DD_GETVPORTOUTPUTFORMATDATA structure at <i>lpGetOutputFormats</i> is <b>NULL</b>. The driver should write the number of output formats that the VPE object supports in the <b>dwNumFormats</b> member of DD_GETVPORTOUTPUTFORMATDATA. Upon return, DirectDraw will allocate this number of <a href="https://msdn.microsoft.com/bbc26c03-c154-4b1e-883e-2942b59ded02">DDPIXELFORMAT</a> structures to pass in the second call to <b>DdVideoPortGetOutputFormats</b>.

</li>
<li>
In the second call, <b>lpddpfOutputFormats</b> points to the array of allocated DDPIXELFORMAT structures. The driver should fill in each structure with a description of each output format that the VPE object can write to the frame buffer. The driver should return only those output formats that it supports based on the input format of the video data. The driver should also return the number of supported output formats in <b>dwNumFormats</b>. Note that the driver is guaranteed that the buffer to which <b>lpddpfOutputFormats</b> points is large enough to hold the format information being requested.

</li>
</ul>
If the <b>dwFlags</b> member of DD_GETVPORTOUTPUTFORMATDATA is set only to DDVPFORMAT_VIDEO, the driver should return only those output formats that are supported for normal video data. If <b>dwFlags</b> is set only to DDVPFORMAT_VBI, the driver should return only those formats supported for <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> data. If <b>dwFlags</b> is set to both flags, the driver should return all formats supported by the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VPE</a> object.




## -see-also




<a href="https://msdn.microsoft.com/bbc26c03-c154-4b1e-883e-2942b59ded02">DDPIXELFORMAT</a>



<a href="https://msdn.microsoft.com/3033a4e9-3f94-4702-9db8-098a358ab1c2">DD_GETVPORTOUTPUTFORMATDATA</a>
 

 

