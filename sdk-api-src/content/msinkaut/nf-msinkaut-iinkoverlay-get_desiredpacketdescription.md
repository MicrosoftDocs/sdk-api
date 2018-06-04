---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IInkOverlay::get_DesiredPacketDescription


## -description



Gets or sets the desired packet description of the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>.



This property is read/write.


## -parameters


## -remarks



The description is an array of globally unique identifiers (GUIDs) from the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> object.

In multitablet mode, this is the packet description for all of the tablet devices. If any of the devices don't support a known packet description property, the property data is not returned.

By default, <a href="https://msdn.microsoft.com/320cc215-e4e5-4196-8e1b-ca0a30d01d37">DesiredPacketDescription</a> contains <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">STR_GUID_X</a>, STR_GUID_Y, and STR_GUID_NORMALPRESSURE from the PacketProperty object. If you set <b>DesiredPacketDescription</b> to anything else, STR_GUID_BUTTONPRESSURE only for example, STR_GUID_X and STR_GUID_Y is also added. A get of <b>DesiredPacketDescription</b> returns {X,Y,ButtonPressure} and not {ButtonPressure}.

When <a href="https://msdn.microsoft.com/320cc215-e4e5-4196-8e1b-ca0a30d01d37">DesiredPacketDescription</a> is set to something that includes <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">STR_GUID_PAKETSTATUS</a>, the packet status is added in the third position. For example, if you set <b>DesiredPacketDescription</b> to (a, b, c, d, PacketStatus, e, f), when you get <b>DesiredPacketDescription</b> the result is (X, Y, PacketStatus, a, b, c, d, e, f).

Changes to this property do not affect incoming packet data until the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property changes from <b>FALSE</b> to <b>TRUE</b>.




## -see-also




<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>
 

 

