---
UID: NF:rtscom.IRealTimeStylus.GetPacketDescriptionData
title: IRealTimeStylus::GetPacketDescriptionData (rtscom.h)
description: Retrieves the packet properties and scaling factors.
helpviewer_keywords: ["7eff81c6-8ed5-434b-8e78-fcdb952f37e8","GetPacketDescriptionData","GetPacketDescriptionData method [Tablet PC]","GetPacketDescriptionData method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetPacketDescriptionData method","IRealTimeStylus.GetPacketDescriptionData","IRealTimeStylus::GetPacketDescriptionData","rtscom/IRealTimeStylus::GetPacketDescriptionData","tablet.irealtimestylus_getpacketdescriptiondata"]
old-location: tablet\irealtimestylus_getpacketdescriptiondata.htm
tech.root: tablet
ms.assetid: 7eff81c6-8ed5-434b-8e78-fcdb952f37e8
ms.date: 12/05/2018
ms.keywords: 7eff81c6-8ed5-434b-8e78-fcdb952f37e8, GetPacketDescriptionData, GetPacketDescriptionData method [Tablet PC], GetPacketDescriptionData method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetPacketDescriptionData method, IRealTimeStylus.GetPacketDescriptionData, IRealTimeStylus::GetPacketDescriptionData, rtscom/IRealTimeStylus::GetPacketDescriptionData, tablet.irealtimestylus_getpacketdescriptiondata
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
 - IRealTimeStylus::GetPacketDescriptionData
 - rtscom/IRealTimeStylus::GetPacketDescriptionData
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
 - IRealTimeStylus.GetPacketDescriptionData
---

# IRealTimeStylus::GetPacketDescriptionData


## -description

Retrieves the packet properties and scaling factors.

## -parameters

### -param tcid [in]

Specifies the tablet context identifier.

### -param pfInkToDeviceScaleX [in, out]

Specifies the conversion factor for the horizontal axis from ink space to digitizer coordinates.

### -param pfInkToDeviceScaleY [in, out]

Specifies the conversion factor for the vertical axis from ink space to digitizer coordinates.

### -param pcPacketProperties [in, out]

The number of properties in each packet.

### -param ppPacketProperties [out]

Pointer to an array containing the GUIDs and property metrics for each packet property.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

You can pass <b>NULL</b> if you do not want the scaling parameters.

The <b>IRealTimeStylus::GetPacketDescriptionData Method</b> uses <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> to allocate space for <i>ppPacketProperties</i>. The caller should call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when the array is no longer needed.

The order of properties in the stream of data sent to plug-ins is the same as the order of the properties returned by <b>IRealTimeStylus::GetPacketDescriptionData Method</b>. Use this method to determine what the hardware is reporting versus what was requested when calling <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>.


#### Examples

This C++ code example uses the <b>IRealTimeStylus::GetPacketDescriptionData Method</b> method to get information about the ink packet data.


```cpp
STDMETHODIMP CCustomRenderer::StylusUp( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
TABLET_CONTEXT_ID *pTcids;
ULONG ulTcidCount;
TABLET_CONTEXT_ID tcid;
FLOAT fInkToDeviceScaleX;
FLOAT fInkToDeviceScaleY;
ULONG ulPacketProperties;
PACKET_PROPERTY *pPacketProperties;

// Get all the tablet context identifiers
HRESULT hr = piRtsSrc->GetAllTabletContextIds(&ulTcidCount, &pTcids);

// Use the first tablet context identifier in the array
tcid = *pTcids;

// Get the packet description data
hr = piRtsSrc->GetPacketDescriptionData(tcid, &fInkToDeviceScaleX, 
                                        &fInkToDeviceScaleY, &ulPacketProperties,
                                        &pPacketProperties);

// Use the packet description data to do things like scale the ink 
// to the physical display device when rendering your own strokes

	return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getdesiredpacketdescription">IRealTimeStylus::GetDesiredPacketDescription Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>