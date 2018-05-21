---
UID: NN:rtscom.IStrokeBuilder
title: IStrokeBuilder
author: windows-driver-content
description: Use interface to programmatically create strokes from packet data.
old-location: tablet\istrokebuilder.htm
old-project: tablet
ms.assetid: 309fcc8a-6a14-4ee3-b340-5e47ff249bf8
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 309fcc8a-6a14-4ee3-b340-5e47ff249bf8, IStrokeBuilder, IStrokeBuilder interface [Tablet PC], IStrokeBuilder interface [Tablet PC],described, rtscom/IStrokeBuilder, tablet.istrokebuilder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IStrokeBuilder
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStrokeBuilder interface


## -description



Use interface to programmatically create strokes from packet data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStrokeBuilder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStrokeBuilder</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7b53a9b2-11da-4063-aac3-a85e52abeb52">AppendPackets</a>
</td>
<td align="left" width="63%">
Adds a packet to the end of the packet list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40b8ce05-0272-4505-8361-13bb6ca701ea">BeginStroke</a>
</td>
<td align="left" width="63%">
Begins a stroke on an ink object by using packet data from a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7c6f177-3d89-4f27-b2c0-937b08591305">CreateStroke</a>
</td>
<td align="left" width="63%">
Creates strokes on an ink object by using packet data from the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a535cd20-d24a-4044-a757-fb2b593650b9">EndStroke</a>
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

<a href="https://msdn.microsoft.com/ceb8eaea-5059-4386-ad48-63d563ef9731">Ink</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the ink object that is associated with the <a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder</a> object.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the <a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder Class</a>.

The <a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder Class</a> provides an alternative method of creating a stroke for applications that manage the data. It has methods that can be called from <a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">StylusDown</a>, <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">Packets</a>, and <a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">StylusUp</a> notifications.

The following two models are supported.

<ul>
<li>Converting custom stroke information to a stroke in an atomic fashion by using the <a href="https://msdn.microsoft.com/f7c6f177-3d89-4f27-b2c0-937b08591305">IStrokeBuilder::CreateStroke Method</a> method.</li>
<li>Building the stroke by using the <a href="https://msdn.microsoft.com/40b8ce05-0272-4505-8361-13bb6ca701ea">IStrokeBuilder::BeginStroke Method</a>, <a href="https://msdn.microsoft.com/7b53a9b2-11da-4063-aac3-a85e52abeb52">IStrokeBuilder::AppendPackets Method</a>, and <a href="https://msdn.microsoft.com/a535cd20-d24a-4044-a757-fb2b593650b9">IStrokeBuilder::EndStroke Method</a> methods, which mirror the <a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">StylusDown</a>, <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">Packets</a>, and <a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">StylusUp</a> notifications.</li>
</ul>

#### Examples

The following C++ example shows a partial implementation of an <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a> class. The plug-in uses a <a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder</a> object to create a new ink stroke.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// CStrokeBuilderPlugin

// Helper functions
HRESULT CStrokeBuilderPlugin::GetInk(IInkDisp** pInk)
{
	return m_pStrokeBuilder-&gt;get_Ink(pInk);
}

// IStylusAsyncPlugin Interface implementation

STDMETHODIMP CStrokeBuilderPlugin::RealTimeStylusEnabled( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ ULONG cTcidCount,
            /* [size_is][in] */ const TABLET_CONTEXT_ID *pTcids)
{
	// Create an IStrokeBuilder object
	return CoCreateInstance(CLSID_StrokeBuilder, NULL, CLSCTX_INPROC, IID_IStrokeBuilder, (VOID **)&amp;m_pStrokeBuilder);
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
	HRESULT hr = piRtsSrc-&gt;GetPacketDescriptionData(pStylusInfo-&gt;tcid, &amp;fInkToDeviceScaleX, &amp;fInkToDeviceScaleY, 
													&amp;cPacketProperties, &amp;pPacketProperties);

	if (SUCCEEDED(hr))
	{
		// Start creating the stroke
		hr = m_pStrokeBuilder-&gt;BeginStroke(pStylusInfo-&gt;tcid, pStylusInfo-&gt;cid, pPacket, cPropCountPerPkt, 
											pPacketProperties, fInkToDeviceScaleX, fInkToDeviceScaleY, &amp;m_piStroke);
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
	return m_pStrokeBuilder-&gt;AppendPackets(pStylusInfo-&gt;tcid, pStylusInfo-&gt;cid, cPktBuffLength, pPackets);
}

STDMETHODIMP CStrokeBuilderPlugin::StylusUp( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
    // Finish the stroke. This adds the stroke to the StrokeBuilder's Ink object.
    return m_pStrokeBuilder-&gt;EndStroke(pStylusInfo-&gt;tcid, pStylusInfo-&gt;cid, &amp;m_piStroke, NULL);
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/309fcc8a-6a14-4ee3-b340-5e47ff249bf8">IStrokeBuilder Interface</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>
 

 

