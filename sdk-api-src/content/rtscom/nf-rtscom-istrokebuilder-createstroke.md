---
UID: NF:rtscom.IStrokeBuilder.CreateStroke
title: IStrokeBuilder::CreateStroke (rtscom.h)
author: windows-sdk-content
description: Creates strokes on an ink object by using packet data that came from a RealTimeStylus Class object.
old-location: tablet\istrokebuilder_createstroke.htm
tech.root: tablet
ms.assetid: f7c6f177-3d89-4f27-b2c0-937b08591305
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateStroke, CreateStroke method [Tablet PC], CreateStroke method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],CreateStroke method, IStrokeBuilder.CreateStroke, IStrokeBuilder::CreateStroke, f7c6f177-3d89-4f27-b2c0-937b08591305, rtscom/IStrokeBuilder::CreateStroke, tablet.istrokebuilder_createstroke
ms.topic: method
f1_keywords: 
 - "rtscom/IStrokeBuilder.CreateStroke"
dev_langs:
 - c++
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
 - IStrokeBuilder.CreateStroke
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStrokeBuilder::CreateStroke


## -description



Creates strokes on an ink object by using packet data that came from a <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.




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



For a description of the return values, see <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The <i>fInkToDeviceScaleX</i> and <i>fInkToDeviceScaleY</i> parameters affect the internal representation of strokes created with the <b>IStrokeBuilder::CreateStroke Method</b> method. Multiply the x-coordinate in ink space by <i>fInkToDeviceScaleX</i> to get the x-coordinate in digitizer units. Multiply the y-coordinate in ink space by <i>fInkToDeviceScaleY</i> to get the y-coordinate in digitizer units.

To retrieve the scale parameters, use <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getpacketdescriptiondata">IRealTimeStylus::GetPacketDescriptionData Method</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istrokebuilder">IStrokeBuilder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-beginstroke">IStrokeBuilder::BeginStroke Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-endstroke">IStrokeBuilder::EndStroke Method</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/strokebuilder-class">StrokeBuilder Class</a>
 

 

