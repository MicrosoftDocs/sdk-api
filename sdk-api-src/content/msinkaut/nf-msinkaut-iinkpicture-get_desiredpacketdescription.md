---
UID: NF:msinkaut.IInkPicture.get_DesiredPacketDescription
title: IInkPicture::get_DesiredPacketDescription
author: windows-sdk-content
description: Gets or sets the desired packet description of the InkCollector.
old-location: tablet\inkpicture_desiredpacketdescription.htm
tech.root: tablet
ms.assetid: 5b4a667a-b927-4278-9be2-2d7163568582
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DesiredPacketDescription property [Tablet PC], DesiredPacketDescription property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],DesiredPacketDescription property, IInkPicture.DesiredPacketDescription, IInkPicture.get_DesiredPacketDescription, IInkPicture::DesiredPacketDescription, IInkPicture::get_DesiredPacketDescription, IInkPicture::put_DesiredPacketDescription, InkPicture.get_DesiredPacketDescription, InkPicture.put_DesiredPacketDescription, get_DesiredPacketDescription, msinkaut/IInkPicture::DesiredPacketDescription, msinkaut/IInkPicture::get_DesiredPacketDescription, msinkaut/IInkPicture::put_DesiredPacketDescription, putDesiredPacketDescription, tablet.inkpicture_desiredpacketdescription
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkPicture.DesiredPacketDescription
 - IInkPicture.get_DesiredPacketDescription
 - IInkPicture.put_DesiredPacketDescription
 - InkPicture.get_DesiredPacketDescription
 - InkPicture.put_DesiredPacketDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkPicture.get_DesiredPacketDescription
: 
---

# IInkPicture::get_DesiredPacketDescription


## -description



Gets or sets the desired packet description of the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>.



This property is read/write.


## -parameters


## -remarks



The description is an array of globally unique identifiers (GUIDs) from the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> object.

In multitablet mode, this is the packet description for all of the tablet devices. If any of the devices don't support a known packet description property, the property data is not returned.

By default, <b>DesiredPacketDescription</b> contains <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">STR_GUID_X</a>, STR_GUID_Y, and STR_GUID_NORMALPRESSURE from the PacketProperty object. If you set <b>DesiredPacketDescription</b> to anything else, STR_GUID_BUTTONPRESSURE only for example, STR_GUID_X and STR_GUID_Y is also added.  A get of <b>DesiredPacketDescription</b> returns {X,Y,ButtonPressure} and not {ButtonPressure}.

When <b>DesiredPacketDescription</b> is set to something that includes <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">STR_GUID_PAKETSTATUS</a>, the packet status is added in the third position. For example, if you set <b>DesiredPacketDescription</b> to (a, b, c, d, PacketStatus, e, f), when you get <b>DesiredPacketDescription</b> the result is (X, Y, PacketStatus, a, b, c, d, e, f).

Changes to this property do not affect incoming packet data until the <a href="https://msdn.microsoft.com/1c6e9fb4-be51-4d68-8241-17119deeba3f">Enabled</a> property changes from <b>FALSE</b> to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/EA6AC3DD-5F13-442A-B93D-FF0A5333609A">IInkPicture</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>



<a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>
 

 

