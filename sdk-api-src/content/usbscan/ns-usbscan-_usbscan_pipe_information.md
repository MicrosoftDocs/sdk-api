---
UID: NS:usbscan._USBSCAN_PIPE_INFORMATION
title: "_USBSCAN_PIPE_INFORMATION"
author: windows-driver-content
description: The USBSCAN_PIPE_INFORMATION structure is used to describe a USB transfer pipe for a still image device. An array of USBSCAN_PIPE_INFORMATION structures is supplied within a USBSCAN_PIPE_CONFIGURATION structure.
old-location: image\usbscan_pipe_information.htm
old-project: image
ms.assetid: a13bec15-67e1-45f9-be90-dee5c555ad64
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PUSBSCAN_PIPE_INFORMATION, PUSBSCAN_PIPE_INFORMATION, PUSBSCAN_PIPE_INFORMATION structure pointer [Imaging Devices], USBSCAN_PIPE_INFORMATION, USBSCAN_PIPE_INFORMATION structure [Imaging Devices], _USBSCAN_PIPE_INFORMATION, image.usbscan_pipe_information, stifnc_3a31b5a2-4bd9-4e95-b10d-959c6caa8754.xml, usbscan/PUSBSCAN_PIPE_INFORMATION, usbscan/USBSCAN_PIPE_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usbscan.h
req.include-header: Usbscan.h
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
req.typenames: USBSCAN_PIPE_INFORMATION, *PUSBSCAN_PIPE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbscan.h
api_name:
-	USBSCAN_PIPE_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _USBSCAN_PIPE_INFORMATION structure


## -description


The USBSCAN_PIPE_INFORMATION structure is used to describe a USB transfer pipe for a still image device. An array of USBSCAN_PIPE_INFORMATION structures is supplied within a <a href="https://msdn.microsoft.com/library/windows/hardware/ff548541">USBSCAN_PIPE_CONFIGURATION</a> structure.


## -struct-fields




### -field MaximumPacketSize

Maximum packet size for the transfer pipe.


### -field EndpointAddress

The address of the pipe's endpoint. The address is encoded as follows:

<table>
<tr>
<th>Bits</th>
<th>Definition</th>
</tr>
<tr>
<td>
0..3

</td>
<td>
Endpoint number.

</td>
</tr>
<tr>
<td>
4..6

</td>
<td>
Reserved, set to 0.

</td>
</tr>
<tr>
<td>
7

</td>
<td>
Direction, ignored for control endpoints:

0 - OUT endpoint

1 - IN endpoint

</td>
</tr>
</table>
 

For more information, see the <i>Universal Serial Bus Specification</i>.


### -field Interval

Polling interval, in milliseconds, for interrupt pipes. For more information, see the <i>Universal Serial Bus Specification</i>.


### -field PipeType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547001">RAW_PIPE_TYPE</a>-typed value identifying the pipe type.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547001">RAW_PIPE_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548541">USBSCAN_PIPE_CONFIGURATION</a>
 

 

