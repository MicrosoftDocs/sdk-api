---
UID: NF:rtscom.IStrokeBuilder.CreateStroke
title: IStrokeBuilder::CreateStroke
author: windows-driver-content
description: Creates strokes on an ink object by using packet data that came from a RealTimeStylus Class object.
old-location: tablet\istrokebuilder_createstroke.htm
old-project: tablet
ms.assetid: f7c6f177-3d89-4f27-b2c0-937b08591305
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CreateStroke, CreateStroke method [Tablet PC], CreateStroke method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],CreateStroke method, IStrokeBuilder.CreateStroke, IStrokeBuilder::CreateStroke, f7c6f177-3d89-4f27-b2c0-937b08591305, rtscom/IStrokeBuilder::CreateStroke, tablet.istrokebuilder_createstroke
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IStrokeBuilder.CreateStroke
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStrokeBuilder::CreateStroke


## -description



Creates strokes on an ink object by using packet data that came from a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.




## -parameters




### -param cPktBuffLength [in]

The number of LONGs in the <i>pPackets</i> array not the size in bytes. Valid values are between 0 and 0x000FFFFF, inclusive.


### -param pPackets [in]

A pointer to the start of the packet data.


### -param cPacketProperties [in]

The count of longs in the <i>pPacketProperties</i> buffer. This is the number of packets multiplied by the number of properties. Valid values are between 0 and 32, inclusive.


### -param pPacketProperties [in]

The buffer containing the packet properties.


### -param fInkToDeviceScaleX [in]

The horizontal, or x-axis, conversion factor for the horizontal axis from ink space to digitizer coordinates.


### -param fInkToDeviceScaleY [in]

The vertical, or y-axis, conversion factor for the vertical axis from ink space to digitizer coordinates.


### -param ppIInkStroke [in, out]

A pointer to the newly created stroke. This value can be <b>NULL</b>.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The <i>fInkToDeviceScaleX</i> and <i>fInkToDeviceScaleY</i> parameters affect the internal representation of strokes created with the <b>IStrokeBuilder::CreateStroke Method</b> method. Multiply the x-coordinate in ink space by <i>fInkToDeviceScaleX</i> to get the x-coordinate in digitizer units. Multiply the y-coordinate in ink space by <i>fInkToDeviceScaleY</i> to get the y-coordinate in digitizer units.

To retrieve the scale parameters, use <a href="https://msdn.microsoft.com/7eff81c6-8ed5-434b-8e78-fcdb952f37e8">IRealTimeStylus::GetPacketDescriptionData Method</a>.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/309fcc8a-6a14-4ee3-b340-5e47ff249bf8">IStrokeBuilder</a>



<a href="https://msdn.microsoft.com/40b8ce05-0272-4505-8361-13bb6ca701ea">IStrokeBuilder::BeginStroke Method</a>



<a href="https://msdn.microsoft.com/a535cd20-d24a-4044-a757-fb2b593650b9">IStrokeBuilder::EndStroke Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder Class</a>
 

 

