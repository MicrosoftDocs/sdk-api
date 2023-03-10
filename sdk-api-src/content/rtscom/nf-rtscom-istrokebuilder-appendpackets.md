---
UID: NF:rtscom.IStrokeBuilder.AppendPackets
title: IStrokeBuilder::AppendPackets (rtscom.h)
description: Adds a packet to the end of the digitizer input packet list.
helpviewer_keywords: ["7b53a9b2-11da-4063-aac3-a85e52abeb52","AppendPackets","AppendPackets method [Tablet PC]","AppendPackets method [Tablet PC]","IStrokeBuilder interface","IStrokeBuilder interface [Tablet PC]","AppendPackets method","IStrokeBuilder.AppendPackets","IStrokeBuilder::AppendPackets","rtscom/IStrokeBuilder::AppendPackets","tablet.istrokebuilder_appendpackets"]
old-location: tablet\istrokebuilder_appendpackets.htm
tech.root: tablet
ms.assetid: 7b53a9b2-11da-4063-aac3-a85e52abeb52
ms.date: 12/05/2018
ms.keywords: 7b53a9b2-11da-4063-aac3-a85e52abeb52, AppendPackets, AppendPackets method [Tablet PC], AppendPackets method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],AppendPackets method, IStrokeBuilder.AppendPackets, IStrokeBuilder::AppendPackets, rtscom/IStrokeBuilder::AppendPackets, tablet.istrokebuilder_appendpackets
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
 - IStrokeBuilder::AppendPackets
 - rtscom/IStrokeBuilder::AppendPackets
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
 - IStrokeBuilder.AppendPackets
---

# IStrokeBuilder::AppendPackets


## -description

Adds a packet to the end of the digitizer input packet list.

## -parameters

### -param tcid [in]

The context identifier for the tablet device to which the stylus belongs.

### -param sid [in]

The identifier of the stylus object.

### -param cPktBuffLength [in]

The number of LONGs in the <i>pPackets</i> array not the size in bytes. Valid values are between 0 and 0x7FFF, inclusive.

### -param pPackets [in]

The start of the packet data. It is read-only.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method should be called when data packets are sent as a result of the stylus moving while it is touching or in range of the digitizer.

<div class="alert"><b>Note</b>  The incoming packet data is in Himetric format and must be converted to pixels.</div>
<div> </div>

#### Examples

The following C++ example shows the implementation of a <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-packets">IStylusPlugin::Packets Method</a> method on an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a> object. The plug-in uses a <a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder</a> object to create a new ink stroke. The <b>IStrokeBuilder::AppendPackets Method</b> method is called from <b>IStylusPlugin::Packets Method</b> to add new packet data to a stroke in progress as the user drags the stylus across the digitizer.


```cpp
STDMETHODIMP CStrokeBuilderPlugin::Packets( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPktCount,
            /* [in] */ ULONG cPktBuffLength,
            /* [size_is][in] */ LONG *pPackets,
            /* [out][in] */ ULONG *pcInOutPkts,
            /* [out][in] */ LONG **ppInOutPkts)
{
	// Add packet to the stroke
	return m_pStrokeBuilder->AppendPackets(pStylusInfo->tcid, pStylusInfo->cid, cPktBuffLength, pPackets);
}

```

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke">CreateStroke Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istrokebuilder">IStrokeBuilder</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-beginstroke">IStrokeBuilder::BeginStroke Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-endstroke">IStrokeBuilder::EndStroke Method</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder Class</a>