---
UID: NN:rtscom.IStylusPlugin
title: IStylusPlugin
author: windows-sdk-content
description: Receives notifications of RealTimeStylus Class events to enable you to perform custom processing based on those events.
old-location: tablet\istylusplugin.htm
tech.root: tablet
ms.assetid: bbef5cdb-4112-4733-80bb-692b7a198605
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IStylusPlugin, IStylusPlugin interface [Tablet PC], IStylusPlugin interface [Tablet PC],described, bbef5cdb-4112-4733-80bb-692b7a198605, rtscom/IStylusPlugin, tablet.istylusplugin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusPlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStylusPlugin interface


## -description



Receives notifications of <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> events to enable you to perform custom processing based on those events.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStylusPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStylusPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStylusPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d3f556c-b0a8-4346-b7da-82f1a3c2603c">CustomStylusDataAdded</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that custom stylus data is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ff6ccf2-292c-4321-be2a-d6db7ce14943">DataInterest</a>
</td>
<td align="left" width="63%">
Represents the notifications a plug-in is to receive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/236589f8-a6ae-4db3-8be4-68c5babeb9f0">Error</a>
</td>
<td align="left" width="63%">
Notifies the implementing object that this plug-in, one of the previous plug-ins in the <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">StylusAsyncPlugin</a> collection, or a plug-in in the <b>StylusAsyncPlugin</b> collection threw an exception.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ff5f784-33f0-45b8-bccd-3e90a9afd67f">InAirPackets</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen is moving above the digitizer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">Packets</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen is moving on the digitizer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62425c21-62fb-4a29-b024-8d5dc237b430">RealTimeStylusDisabled</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd5689c1-32e2-4a37-8dd2-4525b16f4662">RealTimeStylusEnabled</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60cd2b46-14f7-4a06-a1e7-5b2aa9a1f05c">StylusButtonDown</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the user is pressing a pen button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a56182f3-3e9a-4cc2-895d-54010cd00cb4">StylusButtonUp</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the user has released a pen button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">StylusDown</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen has touched the digitizer surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/586e7fee-6340-46b6-941f-1316b2925e1c">StylusInRange</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the tablet pen is entering the input area of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object or is entering the detection range of the digitizer above the input area of the <b>RealTimeStylus</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd662c32-c226-4dbb-807a-3e560452ef15">StylusOutOfRange</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the pen is leaving the input area of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object or is leaving the detection range of the digitizer above the input area of the <b>RealTimeStylus</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">StylusUp</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in that the user has raised the pen from the tablet digitizer surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cdba29e-0599-45f7-8853-3e8fa29897e8">SystemEvent</a>
</td>
<td align="left" width="63%">
Notifies the implementing plug-in when a system event is received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbc971ad-7cfb-4f75-8d63-a210a7967424">TabletAdded</a>
</td>
<td align="left" width="63%">
Notifies an implementing plug-in when an <a href="https://msdn.microsoft.com/31e11f7d-5610-4c49-9203-2dc322fbef95">ITablet</a> object is attached to the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b953c2f8-3f49-4b7a-af4a-528c8815b066">TabletRemoved</a>
</td>
<td align="left" width="63%">
Notifies an implementing plug-in when an <a href="https://msdn.microsoft.com/31e11f7d-5610-4c49-9203-2dc322fbef95">ITablet</a> object is removed from the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26cefb86-a21e-432d-b3db-1669d5b9cd05">UpdateMapping</a>
</td>
<td align="left" width="63%">
Notifies the implementing object when tablet display properties have changed.

</td>
</tr>
</table> 


## -remarks



Both the <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> and <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> interfaces derive from this interface and can be added to <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> plug-in collections.




## -see-also




<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

