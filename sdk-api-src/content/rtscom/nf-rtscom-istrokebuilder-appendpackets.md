---
UID: NF:rtscom.IStrokeBuilder.AppendPackets
title: IStrokeBuilder::AppendPackets
author: windows-sdk-content
description: Adds a packet to the end of the digitizer input packet list.
old-location: tablet\istrokebuilder_appendpackets.htm
old-project: tablet
ms.assetid: 7b53a9b2-11da-4063-aac3-a85e52abeb52
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: 7b53a9b2-11da-4063-aac3-a85e52abeb52, AppendPackets, AppendPackets method [Tablet PC], AppendPackets method [Tablet PC],IStrokeBuilder interface, IStrokeBuilder interface [Tablet PC],AppendPackets method, IStrokeBuilder.AppendPackets, IStrokeBuilder::AppendPackets, rtscom/IStrokeBuilder::AppendPackets, tablet.istrokebuilder_appendpackets
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStrokeBuilder.AppendPackets
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
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

The number of LONGs in the <i>pPackets</i> array not the size in bytes. Valid values are betwwen 0 and 0x7FFF, inclusive.


### -param pPackets [in]

The start of the packet data. It is read-only.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method should be called when data packets are sent as a result of the stylus moving while it is touching or in range of the digitizer.

<div class="alert"><b>Note</b>  The incoming packet data is in Himetric format and must be converted to pixels.</div>
<div> </div>

#### Examples

The following C++ example shows the implementation of a <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">IStylusPlugin::Packets Method</a> method on an <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a> object. The plug-in uses a <a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder</a> object to create a new ink stroke. The <b>IStrokeBuilder::AppendPackets Method</b> method is called from <b>IStylusPlugin::Packets Method</b> to add new packet data to a stroke in progress as the user drags the stylus across the digitizer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CStrokeBuilderPlugin::Packets( 
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/116c5746-61ad-4a47-a5e3-4675af87b0f1">CreateStroke Method</a>



<a href="https://msdn.microsoft.com/309fcc8a-6a14-4ee3-b340-5e47ff249bf8">IStrokeBuilder</a>



<a href="https://msdn.microsoft.com/40b8ce05-0272-4505-8361-13bb6ca701ea">IStrokeBuilder::BeginStroke Method</a>



<a href="https://msdn.microsoft.com/a535cd20-d24a-4044-a757-fb2b593650b9">IStrokeBuilder::EndStroke Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder Class</a>
 

 

