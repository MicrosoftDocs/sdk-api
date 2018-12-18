---
UID: NC:ddrawint.PDD_VPORTCB_GETBANDWIDTH
title: PDD_VPORTCB_GETBANDWIDTH
author: windows-sdk-content
description: The DdVideoPortGetBandwidth callback function reports the bandwidth limitations of the device's frame buffer memory based the specified VPE object output format.
old-location: display\ddvideoportgetbandwidth.htm
tech.root: display
ms.assetid: 4b9cfec1-a599-47a5-878e-2cde6b3b780a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DdVideoPortGetBandwidth, DdVideoPortGetBandwidth callback function [Display Devices], PDD_VPORTCB_GETBANDWIDTH, PDD_VPORTCB_GETBANDWIDTH callback, ddfncs_e47d95f4-8b95-4344-a1d0-f036007ac802.xml, ddrawint/DdVideoPortGetBandwidth, display.ddvideoportgetbandwidth
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
 - DdVideoPortGetBandwidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_VPORTCB_GETBANDWIDTH callback function


## -description


The <b>DdVideoPortGetBandwidth</b> callback function reports the bandwidth limitations of the device's frame buffer memory based the specified VPE object output format.


## -parameters




### -param Arg1








#### - lpGetVideoPortBandwidth

Points to a <a href="https://msdn.microsoft.com/5a24d819-1498-448a-9360-c14d382059cb">DD_GETVPORTBANDWIDTHDATA</a> structure that contains the information required for the driver to return the bandwidth data.


## -returns



<b>DdVideoPortGetBandwidth</b> returns one of the following callback codes:




## -remarks



<b>DdVideoPortGetBandwidth</b> must be implemented in DirectDraw drivers that support VPE.

<b>DdVideoPortGetBandwidth</b> informs clients of bandwidth requirements for any specified format, helping them to choose a format and better understand its limitations. The driver can supply accurate bandwidth information only after the VPE object has been created because the driver needs the information in the <a href="https://msdn.microsoft.com/efd5907c-ed75-40be-b568-7c305310f79b">DDVIDEOPORTDESC</a> structure.

<b>DdVideoPortGetBandwidth</b> is typically called twice to obtain the bandwidth parameters of the specified hardware video port. Depending on the <b>dwFlags</b> member of the DD_GETVPORTBANDWIDTHDATA structure at <i>lpGetVideoPortBandwidth</i>, the driver should do the following:

<ul>
<li>
When the flag is DDVPB_TYPE, the driver should indicate the type of device it is by setting one of the following flags in the <b>dwCaps</b> member of the <a href="https://msdn.microsoft.com/3e13874d-294e-4161-8131-f78799b2e90e">DDVIDEOPORTBANDWIDTH</a> structure to which the <b>lpBandwidth</b> member of DD_GETVPORTBANDWIDTHDATA points:<ul>
<li>DDVPBCAPS_DESTINATION indicates that the device will describe its bandwidth capabilities in terms of the overlay stretch factor; that is, that the bandwidth information returned by the driver in the next call to <b>DdVideoPortGetBandwidth</b> will refer to the size of the destination overlay. This flag best describes hardware that refreshes from both the primary and overlay surfaces simultaneously. As the destination video is stretched, the hardware has more time to read the pixels from the overlay surface, decreasing the required memory bandwidth.</li>
<li>DDVPBCAPS_SOURCE indicates that the device will describe its bandwidth capabilities in terms of the required source overlay size; that is, that the bandwidth information returned by the next call to <b>DdVideoPortGetBandwidth</b> refers to the size of the source overlay. This flag best describes hardware that prefetches the overlay data into a line buffer or large FIFO. Such hardware does not require extra bandwidth, but does require that the source overlay data fit entirely within the buffer/FIFO size supported by the hardware.</li>
</ul>


The driver should also set the <b>dwSize</b> member of the DDVIDEOPORTBANDWIDTH structure before returning.

</li>
<li>
When the flag is DDVPB_VIDEOPORT, the <b>dwWidth</b> and <b>dwHeight</b> members in the DD_GETVPORTBANDWIDTHDATA structure refer to the prescale size of the video data that the hardware video port will write to the frame buffer as the source overlay. The driver should return an overlay stretch factor at which the device can display the overlay, multiplied by 1000, in each of the <b>dwOverlay</b>, <b>dwColorkey</b>, <b>dwYInterpolate</b>, and <b>dwYInterpAndColorkey</b> members of the DDVIDEOPORTBANDWIDTH structure. For example, a value of 2000 indicates that the device has the bandwidth to stretch the overlay to two times the source's specified size when displaying it. A value of 1000 indicates that no stretching need be done for the specified data size. A value of 500 indicates that the device has sufficient bandwidth to shrink the overlay destination in half. The driver must set a valid value in <b>dwOverlay</b>, but can return -1 in any of the other three members that it does not support.

The DDVPB_VIDEOPORT flag assumes that the device is best described by the DDVPBCAPS_DESTINATION flag. If this is not the case, the driver should fail the call.

</li>
<li>
When the DDVPB_OVERLAY flag is set, the <b>dwWidth</b> and <b>dwHeight</b> members in the DD_GETVPORTBANDWIDTHDATA structure refer to the source overlay size. The driver should return a percentage of this overlay's size, multiplied by 1000, at which it can support displaying the overlay in each of the <b>dwOverlay</b>, <b>dwColorkey</b>, <b>dwYInterpolate</b>, and <b>dwYInterpAndColorkey</b> members of the DDVIDEOPORTBANDWIDTH structure. For example, a value of 750 indicates that the device requires the specified source overlay to be shrunk to 75% of its original size in order for the device to successfully display it. A value of 1000 indicates that no shrinking is required. Drivers for this type of device do not typically return a value greater than 1000. The driver must set a valid value in <b>dwOverlay</b>, but can return 0 in any of the other three members if it does not support color keying and/or Y-axis interpolation.

The DDVPB_OVERLAY flag assumes that the device is best described using the DDVPBCAPS_SOURCE flag. If this is not the case, the driver should fail the call.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e13874d-294e-4161-8131-f78799b2e90e">DDVIDEOPORTBANDWIDTH</a>



<a href="https://msdn.microsoft.com/efd5907c-ed75-40be-b568-7c305310f79b">DDVIDEOPORTDESC</a>



<a href="https://msdn.microsoft.com/5a24d819-1498-448a-9360-c14d382059cb">DD_GETVPORTBANDWIDTHDATA</a>



<a href="https://msdn.microsoft.com/eeaf3cda-6220-4e8e-8f9e-9f52d1b05ab7">DdVideoPortCreate</a>
 

 

