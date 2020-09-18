---
UID: NN:rtscom.IStrokeBuilder
title: IStrokeBuilder (rtscom.h)
description: Use interface to programmatically create strokes from packet data.
helpviewer_keywords: ["309fcc8a-6a14-4ee3-b340-5e47ff249bf8","IStrokeBuilder","IStrokeBuilder interface [Tablet PC]","IStrokeBuilder interface [Tablet PC]","described","rtscom/IStrokeBuilder","tablet.istrokebuilder"]
old-location: tablet\istrokebuilder.htm
tech.root: tablet
ms.assetid: 309fcc8a-6a14-4ee3-b340-5e47ff249bf8
ms.date: 12/05/2018
ms.keywords: 309fcc8a-6a14-4ee3-b340-5e47ff249bf8, IStrokeBuilder, IStrokeBuilder interface [Tablet PC], IStrokeBuilder interface [Tablet PC],described, rtscom/IStrokeBuilder, tablet.istrokebuilder
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
 - IStrokeBuilder
 - rtscom/IStrokeBuilder
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
 - IStrokeBuilder
---

# IStrokeBuilder interface


## -description

Use interface to programmatically create strokes from packet data.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStrokeBuilder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStrokeBuilder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IStrokeBuilder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-appendpackets">AppendPackets</a>
</td>
<td align="left" width="63%">
Adds a packet to the end of the packet list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-beginstroke">BeginStroke</a>
</td>
<td align="left" width="63%">
Begins a stroke on an ink object by using packet data from a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-createstroke">CreateStroke</a>
</td>
<td align="left" width="63%">
Creates strokes on an ink object by using packet data from the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-endstroke">EndStroke</a>
</td>
<td align="left" width="63%">
Ends a stroke and returns the stroke object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStrokeBuilder</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-get_ink">Ink</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the ink object that is associated with the <a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder</a> object.

</td>
</tr>
</table>

## -remarks

This interface is implemented by the <a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder Class</a>.

The <a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder Class</a> provides an alternative method of creating a stroke for applications that manage the data. It has methods that can be called from <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">StylusDown</a>, <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-packets">Packets</a>, and <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusup">StylusUp</a> notifications.

The following two models are supported.

<ul>
<li>Converting custom stroke information to a stroke in an atomic fashion by using the <a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-createstroke">IStrokeBuilder::CreateStroke Method</a> method.</li>
<li>Building the stroke by using the <a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-beginstroke">IStrokeBuilder::BeginStroke Method</a>, <a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-appendpackets">IStrokeBuilder::AppendPackets Method</a>, and <a href="/windows/desktop/api/rtscom/nf-rtscom-istrokebuilder-endstroke">IStrokeBuilder::EndStroke Method</a> methods, which mirror the <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">StylusDown</a>, <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-packets">Packets</a>, and <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusup">StylusUp</a> notifications.</li>
</ul>

#### Examples

The following C++ example shows a partial implementation of an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a> class. The plug-in uses a <a href="/windows/desktop/tablet/strokebuilder-class">StrokeBuilder</a> object to create a new ink stroke.


```cpp
// CStrokeBuilderPlugin

// Helper functions
HRESULT CStrokeBuilderPlugin::GetInk(IInkDisp** pInk)
{
	return m_pStrokeBuilder->get_Ink(pInk);
}

// IStylusAsyncPlugin Interface implementation

STDMETHODIMP CStrokeBuilderPlugin::RealTimeStylusEnabled( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ ULONG cTcidCount,
            /* [size_is][in] */ const TABLET_CONTEXT_ID *pTcids)
{
	// Create an IStrokeBuilder object
	return CoCreateInstance(CLSID_StrokeBuilder, NULL, CLSCTX_INPROC, IID_IStrokeBuilder, (VOID **)&m_pStrokeBuilder);
}

STDMETHODIMP CStrokeBuilderPlugin::DataInterest( 
            /* [retval][out] */ RealTimeStylusDataInterest *pDataInterest)
{
	// Set up the messages we want to receive
	*pDataInterest = (RealTimeStylusDataInterest)(RTSDI_StylusDown | RTSDI_Packets |
                                                  RTSDI_StylusUp | RTSDI_Error);
	return S_OK;
}

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

STDMETHODIMP CStrokeBuilderPlugin::StylusUp( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
    // Finish the stroke. This adds the stroke to the StrokeBuilder's Ink object.
    return m_pStrokeBuilder->EndStroke(pStylusInfo->tcid, pStylusInfo->cid, &m_piStroke, NULL);
}

STDMETHODIMP CStrokeBuilderPlugin::Error( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ IStylusPlugin *piPlugin,
            /* [in] */ RealTimeStylusDataInterest dataInterest,
            /* [in] */ HRESULT hrErrorCode,
            /* [out][in] */ LONG_PTR *lptrKey)
{
	CString strError;
	strError.Format(L"An error occurred. Error code: %d", hrErrorCode);
	TRACE(strError);
	return S_OK;
}

// The remaining interface methods are not used

```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istrokebuilder">IStrokeBuilder Interface</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>