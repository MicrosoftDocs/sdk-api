---
UID: NN:strmif.IVMRMonitorConfig
title: IVMRMonitorConfig
author: windows-sdk-content
description: The IVMRMonitorConfig interface is implemented by the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrmonitorconfig.htm
tech.root: DirectShow
ms.assetid: 02b4016b-a65b-41ac-b5c6-e5f6825f179c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVMRMonitorConfig, IVMRMonitorConfig interface [DirectShow], IVMRMonitorConfig interface [DirectShow],described, IVMRMonitorConfigInterface, dshow.ivmrmonitorconfig, strmif/IVMRMonitorConfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMonitorConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRMonitorConfig interface


## -description



The <code>IVMRMonitorConfig</code> interface is implemented by the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). Applications use this interface to determine the capabilities of the display devices on the system and to control which device is used to display the output. For example, if the system contains a hardware DVD decoder and the VMR is rendering the output from that decoder, then on a multi-monitor system, an application must use this interface to specify the display device that is connected to the decoder.

The VMR-7 supports a maximum of 15 display devices.

It is the responsibility of the application to ensure that the playback window is positioned on the desired monitor before the window is displayed. Otherwise the playback window will be displayed at a location chosen by the Windows Shell (Explorer) which may not be on the desired monitor.

For the VMR-9, use the <a href="https://msdn.microsoft.com/27a3a598-d8de-48b2-8b8c-6b5497db4c6c">IVMRMonitorConfig9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRMonitorConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRMonitorConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRMonitorConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a44ca7d-a195-4fcf-b09c-01f8176e0aa2">GetAvailableMonitors</a>
</td>
<td align="left" width="63%">
Retrieves information about the monitors currently available on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/354b7f6e-35f8-4824-b5b5-24a37166462b">GetDefaultMonitor</a>
</td>
<td align="left" width="63%">
Retrieves the default monitor that all future instances of the VMR will use for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d71f1d1-4f8b-4ff8-9a4f-d25050821622">GetMonitor</a>
</td>
<td align="left" width="63%">
Retrieves the monitor that this instance of the VMR is using for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85757536-ab7d-4b68-9e04-cf04fc4ebd5e">SetDefaultMonitor</a>
</td>
<td align="left" width="63%">
Specifies the default monitor that all future instances of the VMR should use for video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d443592e-23d8-425c-9f88-f4f786fb19c6">SetMonitor</a>
</td>
<td align="left" width="63%">
On a multi-monitor system, specifies the monitor that this instance of the VMR should use for video playback.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

