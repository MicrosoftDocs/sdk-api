---
UID: NN:vmr9.IVMRMonitorConfig9
title: IVMRMonitorConfig9
author: windows-driver-content
description: The IVMRMonitorConfig9 interface is implemented by the Video Mixing Renderer Filter 9 (VMR-9).
old-location: dshow\ivmrmonitorconfig9.htm
old-project: DirectShow
ms.assetid: 27a3a598-d8de-48b2-8b8c-6b5497db4c6c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IVMRMonitorConfig9, IVMRMonitorConfig9 interface [DirectShow], IVMRMonitorConfig9 interface [DirectShow], described, IVMRMonitorConfig9Interface, dshow.ivmrmonitorconfig9, vmr9/IVMRMonitorConfig9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRMonitorConfig9
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRMonitorConfig9 interface


## -description



The <code>IVMRMonitorConfig9</code> interface is implemented by the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9). Applications use this interface to determine the capabilities of the display devices on the system and to control which device is used to display the output. For example, if the system contains a hardware DVD decoder and the VMR is rendering the output from that decoder, then on a multi-monitor system, an application must use this interface to specify the display device that is connected to the decoder.

The VMR-9 supports a maximum of 16 display devices.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRMonitorConfig9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRMonitorConfig9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRMonitorConfig9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cebd40c2-ea41-4ed1-87d1-37f9d427c539">GetAvailableMonitors</a>
</td>
<td align="left" width="63%">
Retrieves information about the monitors currently available on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5d5bf77-5261-42eb-b79b-d72dfb2d9f21">GetDefaultMonitor</a>
</td>
<td align="left" width="63%">
Retrieves the default monitor that all future instances of the VMR will use for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b3e19d2-23de-42ae-9e5b-d53e24bb764a">GetMonitor</a>
</td>
<td align="left" width="63%">
Retrieves the monitor that this instance of the VMR is using for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e02e0b6-8c0e-4c32-9059-91b1b8be165f">SetDefaultMonitor</a>
</td>
<td align="left" width="63%">
Specifies the default monitor that all future instances of the VMR should use for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21b0db95-3b70-4d9a-b533-393e89e106ae">SetMonitor</a>
</td>
<td align="left" width="63%">
On a multi-monitor system, specifies the monitor that this instance of the VMR should use for video playback.

</td>
</tr>
</table> 


## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

