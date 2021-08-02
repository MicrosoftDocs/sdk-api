---
UID: NF:rtscom.IStylusPlugin.Packets
title: IStylusPlugin::Packets (rtscom.h)
description: Notifies the object implementing the plug-in that the tablet pen is moving on the digitizer.
helpviewer_keywords: ["IStylusPlugin interface [Tablet PC]","Packets method","IStylusPlugin.Packets","IStylusPlugin::Packets","Packets","Packets method [Tablet PC]","Packets method [Tablet PC]","IStylusPlugin interface","c6a3d563-4776-4ac6-bdc3-798192ba4546","rtscom/IStylusPlugin::Packets","tablet.istylusplugin_packets"]
old-location: tablet\istylusplugin_packets.htm
tech.root: tablet
ms.assetid: c6a3d563-4776-4ac6-bdc3-798192ba4546
ms.date: 12/05/2018
ms.keywords: IStylusPlugin interface [Tablet PC],Packets method, IStylusPlugin.Packets, IStylusPlugin::Packets, Packets, Packets method [Tablet PC], Packets method [Tablet PC],IStylusPlugin interface, c6a3d563-4776-4ac6-bdc3-798192ba4546, rtscom/IStylusPlugin::Packets, tablet.istylusplugin_packets
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
 - IStylusPlugin::Packets
 - rtscom/IStylusPlugin::Packets
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
 - IStylusPlugin.Packets
---

# IStylusPlugin::Packets


## -description

Notifies the object implementing the plug-in that the tablet pen is moving on the digitizer.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

### -param pStylusInfo [in]

A <a href="/windows/desktop/api/rtscom/ns-rtscom-stylusinfo">StylusInfo Structure</a> structure which contains information about the RTS that is associated with the pen.

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

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Occurs when the pen is moving and is touching the digitizer surface. Use this notification to constrain the packet data within a specified rectangle. Packets used by the <b>IStylusPlugin::Packets Method</b> and <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-inairpackets">IStylusPlugin::InAirPackets Method</a> methods can be deleted.

You can return an array of modified packets by using the <i>ppInOutPkt</i> parameter.

Packets can be bundled in order to make the data transfer more efficient, such that a plug-in is not required to be called once per packet. <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-inairpackets">IStylusPlugin::InAirPackets Method</a> and <b>IStylusPlugin::Packets Method</b> can send one or more packets.


#### Examples

The following C++ code example implements a <b>IStylusPlugin::Packets Method</b> method that modifies the X,Y data to restrain the packets to a rectangle. This is the same functionality that is implemented in C# in the <a href="/windows/desktop/tablet/realtimestylus-plug-in-sample">RealTimeStylus Plug-in Sample</a>.


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

	// Allocate memory for modified packets
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

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<b>IStylusPlugin Interface</b>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">IStylusPlugin::StylusDown Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusup">IStylusPlugin::StylusUp Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>