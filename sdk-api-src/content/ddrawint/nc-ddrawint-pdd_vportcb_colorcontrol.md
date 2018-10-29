---
UID: NC:ddrawint.PDD_VPORTCB_COLORCONTROL
title: PDD_VPORTCB_COLORCONTROL
author: windows-sdk-content
description: The DdVideoPortColorControl callback function gets or sets the VPE object color controls.
old-location: display\ddvideoportcolorcontrol.htm
tech.root: display
ms.assetid: 0d4d5157-cadf-4b63-aafc-ccb252cec2b4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DdVideoPortColorControl, DdVideoPortColorControl callback function [Display Devices], PDD_VPORTCB_COLORCONTROL, PDD_VPORTCB_COLORCONTROL callback, ddfncs_42f1c569-d463-4c22-af43-fb4d829843ab.xml, ddrawint/DdVideoPortColorControl, display.ddvideoportcolorcontrol
ms.prod: windows
ms.technology: windows-sdk
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
 - DdVideoPortColorControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_VPORTCB_COLORCONTROL callback function


## -description


The <b>DdVideoPortColorControl</b> callback function gets or sets the VPE object color controls.


## -parameters




### -param Arg1








#### - lpColorControl

Points to a <a href="https://msdn.microsoft.com/b52bbd7e-2c80-4cfb-b0c5-7900993f4a3a">DD_VPORTCOLORDATA</a> structure that contains the information required for the driver to get the current VPE object color controls or to set new values.


## -returns



<b>DdVideoPortColorControl</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that set the DDVPCAPS_COLORCONTROL flag in the <a href="https://msdn.microsoft.com/ea85f189-7308-48ad-b159-1809749f8183">DDVIDEOPORTCAPS</a> structure must implement <b>DdVideoPortColorControl</b>.

Depending on the value of the <b>dwFlags</b> member of the DD_VPORTCOLORDATA structure at <i>lpColorControl</i>, the driver should do the following:

<ul>
<li>
When <b>dwFlags</b> is DDRAWI_VPORTGETCOLOR, the driver should fill in each member of the <a href="https://msdn.microsoft.com/77c19de1-a046-4752-b9af-a9865861a493">DDCOLORCONTROL</a> structure that it supports with the VPE object's current color control setting. The driver must set the corresponding bit in the <b>dwFlags</b> member of DDCOLORCONTROL for every color control member in which it writes data.

<b>DdVideoPortColorControl</b> can be called to determine the color control capabilities of the VPE object. The driver should therefore fail the call if it does not support a requested color control capability.

</li>
<li>
When <b>dwFlags</b> is DDRAWI_VPORTSETCOLOR, the driver should set the VPE object's color control settings to the values specified in the DDCOLORCONTROL structure. The driver should check the <b>dwFlags</b> member of DDCOLORCONTROL to determine which structure members contain valid data.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/77c19de1-a046-4752-b9af-a9865861a493">DDCOLORCONTROL</a>



<a href="https://msdn.microsoft.com/ea85f189-7308-48ad-b159-1809749f8183">DDVIDEOPORTCAPS</a>



<a href="https://msdn.microsoft.com/b52bbd7e-2c80-4cfb-b0c5-7900993f4a3a">DD_VPORTCOLORDATA</a>
 

 

