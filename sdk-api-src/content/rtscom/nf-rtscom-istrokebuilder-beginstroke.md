---
UID: NF:rtscom.IStrokeBuilder.BeginStroke
title: IStrokeBuilder::BeginStroke
author: windows-sdk-content
description: Begins a stroke on an ink object by using packet data from a RealTimeStylus Class object.
old-location: tablet\istrokebuilder_beginstroke.htm
tech.root: tablet
ms.assetid: 40b8ce05-0272-4505-8361-13bb6ca701ea
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: 40b8ce05-0272-4505-8361-13bb6ca701ea, BeginStroke, BeginStroke method [Tablet PC], BeginStroke method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],BeginStroke method, IStrokeBuilder.BeginStroke, IStrokeBuilder::BeginStroke, rtscom/IStrokeBuilder::BeginStroke, tablet.istrokebuilder_beginstroke
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
 - IStrokeBuilder.BeginStroke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStrokeBuilder::BeginStroke


## -description



Begins a stroke on an ink object by using packet data from a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.




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

A a pointer to the new stroke. This value can be <b>NULL</b>.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Used in conjunction with the <a href="https://msdn.microsoft.com/7b53a9b2-11da-4063-aac3-a85e52abeb52">IStrokeBuilder::AppendPackets Method</a> and <a href="https://msdn.microsoft.com/a535cd20-d24a-4044-a757-fb2b593650b9">IStrokeBuilder::EndStroke Method</a> methods. <b>IStrokeBuilder::BeginStroke Method</b> starts building the stroke. As the motion continues and additional packets are received, the <b>IStrokeBuilder::AppendPackets Method</b> method adds that additional stroke data. When the tablet pen is raised from the surface and there are no more incoming packets, the <b>IStrokeBuilder::EndStroke Method</b> method is called.


#### Examples

The following C++ example shows the implementation of a <a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">IStylusPlugin::StylusDown Method</a> method on an <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a> object. The plug-in uses a <a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder</a> object to create a new ink stroke. The <b>IStrokeBuilder::BeginStroke Method</b> method is called from <b>IStylusPlugin::StylusDown Method</b> to initiate the construction of a stroke.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CStrokeBuilderPlugin::StylusDown( 
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/309fcc8a-6a14-4ee3-b340-5e47ff249bf8">IStrokeBuilder</a>



<a href="https://msdn.microsoft.com/7b53a9b2-11da-4063-aac3-a85e52abeb52">IStrokeBuilder::AppendPackets Method</a>



<a href="https://msdn.microsoft.com/f7c6f177-3d89-4f27-b2c0-937b08591305">IStrokeBuilder::CreateStroke Method</a>



<a href="https://msdn.microsoft.com/a535cd20-d24a-4044-a757-fb2b593650b9">IStrokeBuilder::EndStroke Method</a>



<a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder Class</a>
 

 

