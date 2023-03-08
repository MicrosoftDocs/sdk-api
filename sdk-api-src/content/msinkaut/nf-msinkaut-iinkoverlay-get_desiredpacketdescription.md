---
UID: NF:msinkaut.IInkOverlay.get_DesiredPacketDescription
title: IInkOverlay::get_DesiredPacketDescription (msinkaut.h)
description: Gets or sets the desired packet description of the InkCollector. (IInkOverlay.get_DesiredPacketDescription)
helpviewer_keywords: ["DesiredPacketDescription property [Tablet PC]","DesiredPacketDescription property [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","DesiredPacketDescription property","IInkOverlay.DesiredPacketDescription","IInkOverlay.get_DesiredPacketDescription","IInkOverlay::DesiredPacketDescription","IInkOverlay::get_DesiredPacketDescription","IInkOverlay::put_DesiredPacketDescription","InkOverlay.get_DesiredPacketDescription","InkOverlay.put_DesiredPacketDescription","get_DesiredPacketDescription","msinkaut/IInkOverlay::DesiredPacketDescription","msinkaut/IInkOverlay::get_DesiredPacketDescription","msinkaut/IInkOverlay::put_DesiredPacketDescription","put_DesiredPacketDescription","tablet.inkoverlay_desiredpacketdescription"]
old-location: tablet\inkoverlay_desiredpacketdescription.htm
tech.root: tablet
ms.assetid: 5330adba-6e19-41dd-8f00-ba62be166aad
ms.date: 12/05/2018
ms.keywords: DesiredPacketDescription property [Tablet PC], DesiredPacketDescription property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],DesiredPacketDescription property, IInkOverlay.DesiredPacketDescription, IInkOverlay.get_DesiredPacketDescription, IInkOverlay::DesiredPacketDescription, IInkOverlay::get_DesiredPacketDescription, IInkOverlay::put_DesiredPacketDescription, InkOverlay.get_DesiredPacketDescription, InkOverlay.put_DesiredPacketDescription, get_DesiredPacketDescription, msinkaut/IInkOverlay::DesiredPacketDescription, msinkaut/IInkOverlay::get_DesiredPacketDescription, msinkaut/IInkOverlay::put_DesiredPacketDescription, put_DesiredPacketDescription, tablet.inkoverlay_desiredpacketdescription
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkOverlay::get_DesiredPacketDescription
 - msinkaut/IInkOverlay::get_DesiredPacketDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.DesiredPacketDescription
 - IInkOverlay.get_DesiredPacketDescription
 - IInkOverlay.put_DesiredPacketDescription
 - InkOverlay.get_DesiredPacketDescription
 - InkOverlay.put_DesiredPacketDescription
---

# IInkOverlay::get_DesiredPacketDescription


## -description

Gets or sets the desired packet description of the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>.



This property is read/write.

## -parameters

## -remarks

The description is an array of globally unique identifiers (GUIDs) from the <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketProperty</a> object.

In multitablet mode, this is the packet description for all of the tablet devices. If any of the devices don't support a known packet description property, the property data is not returned.

By default, <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription">DesiredPacketDescription</a> contains <a href="/windows/desktop/tablet/packetpropertyguids-constants">STR_GUID_X</a>, STR_GUID_Y, and STR_GUID_NORMALPRESSURE from the PacketProperty object. If you set <b>DesiredPacketDescription</b> to anything else, STR_GUID_BUTTONPRESSURE only for example, STR_GUID_X and STR_GUID_Y is also added. A get of <b>DesiredPacketDescription</b> returns {X,Y,ButtonPressure} and not {ButtonPressure}.

When <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription">DesiredPacketDescription</a> is set to something that includes <a href="/windows/desktop/tablet/packetpropertyguids-constants">STR_GUID_PAKETSTATUS</a>, the packet status is added in the third position. For example, if you set <b>DesiredPacketDescription</b> to (a, b, c, d, PacketStatus, e, f), when you get <b>DesiredPacketDescription</b> the result is (X, Y, PacketStatus, a, b, c, d, e, f).

Changes to this property do not affect incoming packet data until the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property changes from <b>FALSE</b> to <b>TRUE</b>.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketPropertyGuids Constants</a>
