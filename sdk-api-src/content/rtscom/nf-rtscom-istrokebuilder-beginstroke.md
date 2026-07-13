---
UID: NF:rtscom.IStrokeBuilder.BeginStroke
title: IStrokeBuilder::BeginStroke (rtscom.h)
description: Begins a stroke on an ink object by using packet data from a RealTimeStylus Class object.
helpviewer_keywords: ["40b8ce05-0272-4505-8361-13bb6ca701ea","BeginStroke","BeginStroke method [Tablet PC]","BeginStroke method [Tablet PC]","IStrokeBuilder interface","IStrokeBuilder interface [Tablet PC]","BeginStroke method","IStrokeBuilder.BeginStroke","IStrokeBuilder::BeginStroke","rtscom/IStrokeBuilder::BeginStroke","tablet.istrokebuilder_beginstroke"]
old-location: tablet\istrokebuilder_beginstroke.htm
tech.root: tablet
ms.assetid: 40b8ce05-0272-4505-8361-13bb6ca701ea
ms.date: 12/05/2018
ms.keywords: 40b8ce05-0272-4505-8361-13bb6ca701ea, BeginStroke, BeginStroke method [Tablet PC], BeginStroke method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],BeginStroke method, IStrokeBuilder.BeginStroke, IStrokeBuilder::BeginStroke, rtscom/IStrokeBuilder::BeginStroke, tablet.istrokebuilder_beginstroke
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStrokeBuilder::BeginStroke
 - rtscom/IStrokeBuilder::BeginStroke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStrokeBuilder.BeginStroke
---

# IStrokeBuilder::BeginStroke


## -description

Begins a stroke on an ink object by using packet data from a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

## -parameters

### -param tcid [in]

The tablet context identifier.

### -param sid [in]

The stylus identifier.

### -param pPacket [in]

The start of the packet data. It is read-only.

### -param cPacketProperties [in]

The count of LONGs, which is the number of packets multiplied by the number of properties, in the <i>pPacketProperties</i> buffer.

### -param pPacketProperties [in]

The buffer containing the packet properties.

### -param fInkToDeviceScaleX [in]

The horizontal, or x-axis, conversion factor for the horizontal axis from ink space to digitizer coordinates.

### -param fInkToDeviceScaleY [in]

The vertical, or y-axis, conversion factor for the vertical axis from ink space to digitizer coordinates.

### -param ppIInkStroke [in, out]

A pointer to the new stroke. This value can be <b>NULL</b>.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Used in conjunction with the <a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-appendpackets">IStrokeBuilder::AppendPackets Method</a> and <a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-endstroke">IStrokeBuilder::EndStroke Method</a> methods. <b>IStrokeBuilder::BeginStroke Method</b> starts building the stroke. As the motion continues and additional packets are received, the <b>IStrokeBuilder::AppendPackets Method</b> method adds that additional stroke data. When the tablet pen is raised from the surface and there are no more incoming packets, the <b>IStrokeBuilder::EndStroke Method</b> method is called.


#### Examples

The following C++ example shows the implementation of a <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">IStylusPlugin::StylusDown Method</a> method on an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a> object. The plug-in uses a <a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder</a> object to create a new ink stroke. The <b>IStrokeBuilder::BeginStroke Method</b> method is called from <b>IStylusPlugin::StylusDown Method</b> to initiate the construction of a stroke.


```cpp
STDMETHODIMP CStrokeBuilderPlugin::StylusDown( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
	FLOAT fInkToDeviceScaleX;
	FLOAT fInkToDeviceScaleY;
	ULONG cPacketProperties;
	PACKET_PROPERTY* pPacketProperties;

	// Get the info we need to call BeginStroke
	HRESULT hr = piRtsSrc->GetPacketDescriptionData(pStylusInfo->tcid, &fInkToDeviceScaleX, &fInkToDeviceScaleY, 
													&cPacketProperties, &pPacketProperties);

	if (SUCCEEDED(hr))
	{
		// Start creating the stroke
		hr = m_pStrokeBuilder->BeginStroke(pStylusInfo->tcid, pStylusInfo->cid, pPacket, cPropCountPerPkt, 
											pPacketProperties, fInkToDeviceScaleX, fInkToDeviceScaleY, &m_piStroke);
	}
	
	return hr;
}

```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istrokebuilder">IStrokeBuilder</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-appendpackets">IStrokeBuilder::AppendPackets Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-createstroke">IStrokeBuilder::CreateStroke Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-endstroke">IStrokeBuilder::EndStroke Method</a>



<a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder Class</a>