---
UID: NF:rtscom.IStylusPlugin.StylusUp
title: IStylusPlugin::StylusUp (rtscom.h)
description: Notifies the implementing plug-in that the user has raised the tablet pen from the tablet digitizer surface.
helpviewer_keywords: ["IStylusPlugin interface [Tablet PC]","StylusUp method","IStylusPlugin.StylusUp","IStylusPlugin::StylusUp","StylusUp","StylusUp method [Tablet PC]","StylusUp method [Tablet PC]","IStylusPlugin interface","b0f9e49c-6a16-43c5-a653-d6142e58019a","rtscom/IStylusPlugin::StylusUp","tablet.istylusplugin_stylusup"]
old-location: tablet\istylusplugin_stylusup.htm
tech.root: tablet
ms.assetid: b0f9e49c-6a16-43c5-a653-d6142e58019a
ms.date: 12/05/2018
ms.keywords: IStylusPlugin interface [Tablet PC],StylusUp method, IStylusPlugin.StylusUp, IStylusPlugin::StylusUp, StylusUp, StylusUp method [Tablet PC], StylusUp method [Tablet PC],IStylusPlugin interface, b0f9e49c-6a16-43c5-a653-d6142e58019a, rtscom/IStylusPlugin::StylusUp, tablet.istylusplugin_stylusup
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
 - IStylusPlugin::StylusUp
 - rtscom/IStylusPlugin::StylusUp
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
 - IStylusPlugin.StylusUp
---

# IStylusPlugin::StylusUp


## -description

Notifies the implementing plug-in that the user has raised the tablet pen from the tablet digitizer surface.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object that sent the notification.

### -param pStylusInfo [in]

A <a href="/windows/desktop/api/rtscom/ns-rtscom-stylusinfo">StylusInfo Structure</a> containing the information about the RTS that is associated with the pen.

### -param cPropCountPerPkt [in]

Number of properties per packet. Valid values are 0 through 32, inclusive.

### -param pPacket [in]

The start of the packet data.

### -param ppInOutPkt [in, out]

A pointer to the modified stylus data packet. The plug-in can use this parameter to feed modified packet data to downstream packets. A value other than <b>NULL</b> indicates that the packet has been modified and RTS will send this data down to plug-ins by using the <i>pPacket</i> parameter.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method is used when the pen leaves the digitizer surface.

You can return an array of modified packets in the buffer, <i>ppInOutPkt</i>. Packets used by the <b>IStylusPlugin::StylusUp Method</b> and <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">IStylusPlugin::StylusDown Method</a> methods can only be modified. They cannot be deleted. Packets used by the <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-packets">IStylusPlugin::Packets Method</a> and <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-inairpackets">IStylusPlugin::InAirPackets Method</a> methods can be deleted.

If you modify packets, then <i>cPropCountPerPkt</i>, which is the number of LONGs in <i>ppInOutPkt</i>, must be divisible by the current desired packet properties (DPP) available on the current input device.

You modify packets by updating the <i>cPropCountPerPkt</i> and <i>ppInOutPkts</i> parameters. Change <i>cPropCountPerPkt</i> to a valid total packet property count and <i>ppInOutPkts</i> to a valid data buffer accounting for values for each DPP in every packet. Only one packet can be present at that location for <b>IStylusPlugin::StylusUp Method</b> and <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">IStylusPlugin::StylusDown Method</a>.

For example, if you add three packets and your DPP is currently X,Y and Pressure, then you must have nine LONG values in this buffer and set <i>cPropCountPerPkt</i> to 9.

The <i>cPropCountPerPkt</i> value is useful to help clarify the boundaries between packets in the flat array of integers that comes in for events such as the <a href="/windows/desktop/tablet/inkcollector-newpackets">NewPackets Event</a> event. Packets can be bundled in order to be more efficient with data transfer, such that it is not required that a plug-is called once per packet.


#### Examples

The following C++ code example implements a <b>StylusUp</b> method that calls a helper function, <b>ModifyPacket</b>, to change the value of the X,Y data to make it fall within a specified rectangle. This is the same functionality that is implemented in the C# sample, <a href="/windows/desktop/tablet/realtimestylus-plug-in-sample">RealTimeStylus Plug-in Sample</a>. The second code snippet is the <b>ModifyPacket</b> function.


```cpp
STDMETHODIMP CPacketModifier::StylusUp( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
	return ModifyPacket(cPropCountPerPkt, pPacket, ppInOutPkt);
}

```



```cpp
// Helper method to modify a single packet
// Called from StylusDown() and StylusUp()
HRESULT CPacketModifier::ModifyPacket(
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
	// Pointer to a buffer to hold changed packet values
	LONG* pTempOutPkt = NULL;
	
	// X and Y come first (0 and 1), 
	// other properties follow
	ULONG iOtherProps = 2;

	if (cPropCountPerPkt > 0)
	{
		pTempOutPkt = (LONG*)CoTaskMemAlloc(sizeof(LONG)*cPropCountPerPkt);

		if (NULL != pTempOutPkt)
		{
			// Packet data always has x followed by y followed by the rest.
			LONG x = pPacket[0];
			LONG y = pPacket[1];

			// In the packet data, check whether
			// its X,Y values fall outside of the specified rectangle.
			// If so, replace them with the nearest point that still
			// falls within the rectangle.
			x = (x < m_filterRect.left ? m_filterRect.left : x);
			x = (x > m_filterRect.right ? m_filterRect.right : x);
			y = (y < m_filterRect.top ? m_filterRect.top : y);
			y = (y > m_filterRect.bottom ? m_filterRect.bottom : y);

			// If necessary, modify the x,y packet data
			if ((x != pPacket[0]) || (y != pPacket[1]))
			{
				pTempOutPkt[0] = x;
				pTempOutPkt[1] = y;

				// Copy the properties that we haven't modified
				while (iOtherProps < cPropCountPerPkt)
				{
					pTempOutPkt[iOtherProps] = pPacket[iOtherProps++];
				}

				*ppInOutPkt = pTempOutPkt;
			}
			else
			{
				CoTaskMemFree(pTempOutPkt);
			}
		}
	}

	return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>