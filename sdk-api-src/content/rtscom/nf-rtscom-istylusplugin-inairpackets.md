---
UID: NF:rtscom.IStylusPlugin.InAirPackets
title: IStylusPlugin::InAirPackets
author: windows-sdk-content
description: Notifies the object implementing the plug-in that the stylus is moving above the digitizer.
old-location: tablet\istylusplugin_inairpackets.htm
tech.root: tablet
ms.assetid: 9ff5f784-33f0-45b8-bccd-3e90a9afd67f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 9ff5f784-33f0-45b8-bccd-3e90a9afd67f, IStylusPlugin interface [Tablet PC],InAirPackets method, IStylusPlugin.InAirPackets, IStylusPlugin::InAirPackets, InAirPackets, InAirPackets method [Tablet PC], InAirPackets method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::InAirPackets, tablet.istylusplugin_inairpackets
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
 - IStylusPlugin.InAirPackets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStylusPlugin::InAirPackets


## -description



Notifies the object implementing the plug-in that the stylus is moving above the digitizer.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param pStylusInfo [in]

A <a href="https://msdn.microsoft.com/d2642082-e18c-4f91-b08c-e25aa388a2a3">StylusInfo Structure</a> structure containing the information about the RTS that is associated with the stylus.


### -param cPktCount [in]

The number of properties per data packet.


### -param cPktBuffLength [in]

The length, in <b>bytes</b>, of the buffer pointed to by <i>pPackets</i>. The memory occupied by each packet is (<i>cPktBuffLength</i> / <i>cPktCount</i>). Valid values are 0 through 0x7FFF, inclusive.


### -param pPackets [in]

A pointer to the start of the packet data. It is read-only.


### -param pcInOutPkts [in, out]

The number of <b>LONGs</b> in <i>ppInOutPkt</i>.


### -param ppInOutPkts [in, out]

A pointer to an array of modified stylus data packets. The plug-in can use this parameter to feed modified packet data to downstream packets. For a value other than <b>NULL</b>, RTS will send this data down to plug-ins by using the <i>pPacket</i> parameter.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/712908e1-2d1d-4e42-8c80-71354b03d318">Classes and Interfaces - Ink Analysis</a>.




## -remarks



This method is called when data packets are created by the stylus when it is in range but is moving above the digitizer and not touching the digitizer. You can return an array of modified packets by using the <i>ppInOutPkt</i> parameter. Create a buffer and point <i>ppInOutPkts</i> to it. Only one packet can be present at that location.

<div class="alert"><b>Note</b>  Packets used by the <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">IStylusPlugin::Packets Method</a> and <b>IStylusPlugin::InAirPackets Method</b> methods can be deleted.</div>
<div> </div>
A stylus plug-in may be associated with a single RTS or with many. Use the <i>piRtsSrc</i> parameter in the following cases:

<ul>
<li>When the notification requires that the plug-in acquires more information about the specific digitizer from which the notification originated.</li>
<li>When you input additional custom notifications through the system.</li>
</ul>
Packets can be bundled for more efficient data transfer. Therefore a plug-in is not required to be called once per packet. <b>IStylusPlugin::InAirPackets Method</b> and <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">IStylusPlugin::Packets Method</a> can send one or more packets.


#### Examples

The following C++ code example implements a <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">IStylusPlugin::Packets Method</a> method that modifies the X,Y data to restrain the packets to a rectangle. The same code could be applied to an implementation of <b>IStylusPlugin::InAirPackets Method</b>.


```cpp
STDMETHODIMP CPacketModifier::Packets( 
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
	for (ULONG i = 0; i < cPktCount; i += cPropertyCount)
	{
		// Packet data always has X followed by Y 
		// followed by the rest
		LONG x = pPackets[i];
		LONG y = pPackets[i+1];

		// Constrain points to the input rectangle
		x = (x < m_filterRect.left ? m_filterRect.left : x);
		x = (x > m_filterRect.right ? m_filterRect.right : x);
		y = (y < m_filterRect.top ? m_filterRect.top : y);
		y = (y > m_filterRect.bottom ? m_filterRect.bottom : y);

		// If necessary, modify the X,Y packet data
		if ((x != pPackets[i]) || (y != pPackets[i+1]))
		{
			pTempOutPkts[i] = x;
			pTempOutPkts[i+1] = y;
			iOtherProps = i+2;
		
			// Copy the properties that we haven't modified
			while (iOtherProps < (i + cPropertyCount))
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

```





## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">IStylusPlugin::StylusDown Method</a>



<a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">IStylusPlugin::StylusUp Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 

