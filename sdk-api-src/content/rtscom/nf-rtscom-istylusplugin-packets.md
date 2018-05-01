---
UID: NF:rtscom.IStylusPlugin.Packets
title: IStylusPlugin::Packets method
author: windows-driver-content
description: Notifies the object implementing the plug-in that the tablet pen is moving on the digitizer.
old-location: tablet\istylusplugin_packets.htm
old-project: tablet
ms.assetid: c6a3d563-4776-4ac6-bdc3-798192ba4546
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IStylusPlugin, IStylusPlugin interface [Tablet PC], Packets method, IStylusPlugin::Packets, Packets method [Tablet PC], Packets method [Tablet PC], IStylusPlugin interface, Packets,IStylusPlugin.Packets, c6a3d563-4776-4ac6-bdc3-798192ba4546, rtscom/IStylusPlugin::Packets, tablet.istylusplugin_packets
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
-	IStylusPlugin.Packets
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStylusPlugin::Packets method


## -description



Notifies the object implementing the plug-in that the tablet pen is moving on the digitizer.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that sent the notification.


### -param pStylusInfo [in]

A <a href="https://msdn.microsoft.com/d2642082-e18c-4f91-b08c-e25aa388a2a3">StylusInfo Structure</a> structure which contains information about the RTS that is associated with the pen.


### -param cPktCount [in]

The number of properties per data packet.


### -param cPktBuffLength [in]

The length, in <b>bytes</b>, of the buffer pointed to by <i>pPackets</i>. The memory occupied by each packet is (<i>cPktBuffLength</i> / <i>cPktCount</i>). Valid values are 0 through 0x7FFF, inclusive.


### -param pPackets [in]

A pointer to the start of the packet data. 


### -param pcInOutPkts [in, out]

The number of <b>LONGs</b> in <i>ppInOutPkt</i>.


### -param ppInOutPkts [in, out]

A pointer to an array of modified stylus data packets. The plug-in can use this parameter to feed modified packet data to downstream packets. A value other than <b>NULL</b> indicates that the RTS will send this data to plug-ins by using the <i>pPacket</i> parameter.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Occurs when the pen is moving and is touching the digitizer surface. Use this notification to constrain the packet data within a specified rectangle. Packets used by the <b>IStylusPlugin::Packets Method</b> and <a href="https://msdn.microsoft.com/9ff5f784-33f0-45b8-bccd-3e90a9afd67f">IStylusPlugin::InAirPackets Method</a> methods can be deleted.

You can return an array of modified packets by using the <i>ppInOutPkt</i> parameter.

Packets can be bundled in order to make the data transfer more efficient, such that a plug-in is not required to be called once per packet. <a href="https://msdn.microsoft.com/9ff5f784-33f0-45b8-bccd-3e90a9afd67f">IStylusPlugin::InAirPackets Method</a> and <b>IStylusPlugin::Packets Method</b> can send one or more packets.


#### Examples

The following C++ code example implements a <b>IStylusPlugin::Packets Method</b> method that modifies the X,Y data to restrain the packets to a rectangle. This is the same functionality that is implemented in C# in the <a href="https://msdn.microsoft.com/0ba753d1-d81a-4f7a-942c-2967c46febec">RealTimeStylus Plug-in Sample</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CPacketModifier::Packets( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPktCount,
            /* [in] */ ULONG cPktBuffLength,
            /* [size_is][in] */ LONG *pPackets,
            /* [out][in] */ ULONG *pcInOutPkts,
            /* [out][in] */ LONG **ppInOutPkts)
{
	BOOL fModified = FALSE;                             // Did we change the packet data?
	ULONG cPropertyCount = cPktBuffLength/cPktCount;    // # of properties in a packet
	ULONG iOtherProps = 0;                              // Properties other than X and Y

	// Allocate memory for modfied packets
	LONG* pTempOutPkts = (LONG*)CoTaskMemAlloc(sizeof(ULONG)*cPktBuffLength);

	// For each packet in the packet data, check whether
	// its X,Y values fall outside of the specified rectangle.  
	// If so, replace them with the nearest point that still
	// falls within the rectangle.
	for (ULONG i = 0; i &lt; cPktCount; i += cPropertyCount)
	{
		// Packet data always has X followed by Y 
		// followed by the rest
		LONG x = pPackets[i];
		LONG y = pPackets[i+1];

		// Constrain points to the input rectangle
		x = (x &lt; m_filterRect.left ? m_filterRect.left : x);
		x = (x &gt; m_filterRect.right ? m_filterRect.right : x);
		y = (y &lt; m_filterRect.top ? m_filterRect.top : y);
		y = (y &gt; m_filterRect.bottom ? m_filterRect.bottom : y);

		// If necessary, modify the X,Y packet data
		if ((x != pPackets[i]) || (y != pPackets[i+1]))
		{
			pTempOutPkts[i] = x;
			pTempOutPkts[i+1] = y;
			iOtherProps = i+2;
		
			// Copy the properties that we haven't modified
			while (iOtherProps &lt; (i + cPropertyCount))
			{
				pTempOutPkts[iOtherProps] = pPackets[iOtherProps++];
			}

			fModified = TRUE;
		}
	}

	if (fModified)
	{
		// Set the [out] pointer to the 
		// memory we allocated and updated
		*ppInOutPkts = pTempOutPkts;
		*pcInOutPkts = cPktCount;
	}
	else
	{
		// Nothing modified, release the memory we allocated
		CoTaskMemFree(pTempOutPkts);
	}

	return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<b>IStylusPlugin Interface</b>



<a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">IStylusPlugin::StylusDown Method</a>



<a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">IStylusPlugin::StylusUp Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

