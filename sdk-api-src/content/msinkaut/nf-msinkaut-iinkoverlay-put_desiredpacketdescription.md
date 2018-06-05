---
UID: NF:msinkaut.IInkOverlay.put_DesiredPacketDescription
title: IInkOverlay::put_DesiredPacketDescription
author: windows-sdk-content
description: Gets or sets the desired packet description of the InkCollector.
old-location: tablet\inkoverlay_desiredpacketdescription.htm
old-project: tablet
ms.assetid: 5330adba-6e19-41dd-8f00-ba62be166aad
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: DesiredPacketDescription property [Tablet PC], DesiredPacketDescription property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],DesiredPacketDescription property, IInkOverlay.DesiredPacketDescription, IInkOverlay.put_DesiredPacketDescription, IInkOverlay::DesiredPacketDescription, IInkOverlay::get_DesiredPacketDescription, IInkOverlay::put_DesiredPacketDescription, InkOverlay.get_DesiredPacketDescription, InkOverlay.put_DesiredPacketDescription, get_DesiredPacketDescription, msinkaut/IInkOverlay::DesiredPacketDescription, msinkaut/IInkOverlay::get_DesiredPacketDescription, msinkaut/IInkOverlay::put_DesiredPacketDescription, put_DesiredPacketDescription, tablet.inkoverlay_desiredpacketdescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkOverlay.DesiredPacketDescription
-	IInkOverlay.get_DesiredPacketDescription
-	IInkOverlay.put_DesiredPacketDescription
-	InkOverlay.get_DesiredPacketDescription
-	InkOverlay.put_DesiredPacketDescription
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::put_DesiredPacketDescription


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
 

 

