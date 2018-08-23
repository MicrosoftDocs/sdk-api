---
UID: NF:rtscom.IStylusPlugin.StylusDown
title: IStylusPlugin::StylusDown
author: windows-sdk-content
description: Notifies the implementing plug-in that the tablet pen has touched the digitizer surface.
old-location: tablet\istylusplugin_stylusdown.htm
old-project: tablet
ms.assetid: 13fb831c-e3e8-4e04-81ce-d4658be105a0
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 13fb831c-e3e8-4e04-81ce-d4658be105a0, IStylusPlugin interface [Tablet PC],StylusDown method, IStylusPlugin.StylusDown, IStylusPlugin::StylusDown, StylusDown, StylusDown method [Tablet PC], StylusDown method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::StylusDown, tablet.istylusplugin_stylusdown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.redist: 
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
 - IStylusPlugin.StylusDown
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IStylusPlugin::StylusDown


## -description


Notifies the implementing plug-in that the tablet pen has touched the digitizer surface.
        


## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param pStylusInfo [in]

A <a href="https://msdn.microsoft.com/d2642082-e18c-4f91-b08c-e25aa388a2a3">StylusInfo Structure</a> containing the information about the RTS that is associated with the stylus.


### -param cPropCountPerPkt [in]

Number of properties per packet. Valid values are 0 through 32, inclusive.


### -param pPacket [in]

The start of the packet data.
          


### -param ppInOutPkt [in, out]

A pointer to the modified stylus data packet. The plug-in can use this parameter to feed modified packet data to downstream packets. A value other than <b>NULL</b> indicates that the packet has been modified and RTS will send this data down to plug-ins by using the <i>pPacket</i> parameter.


## -returns



For a description of return values, <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



You can return an array of modified packets in the buffer, <i>ppInOutPkt</i>. Packets used by the <a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">IStylusPlugin::StylusUp Method</a> and <b>IStylusPlugin::StylusDown Method</b> methods can only be changed. Packets used by the <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">IStylusPlugin::Packets Method</a> and <a href="https://msdn.microsoft.com/9ff5f784-33f0-45b8-bccd-3e90a9afd67f">IStylusPlugin::InAirPackets Method</a> methods can be deleted.

If you modify packets, then <i>cPropCountPerPkt</i>, which is the number of LONGs in <i>ppInOutPkt</i>, must be divisible by the current desired packet properties (DPP) available on the current input device.

You can modify packets by updating the <i>cPropCountPerPkt</i> and <i>ppInOutPkts</i> parameters. Change <i>cPropCountPerPkt</i> to a valid total packet property count and change <i>ppInOutPkts</i> to pointer to a valid data buffer accounting for values for each DPP in every packet. Only one packet can be present at that location for <a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">IStylusPlugin::StylusUp Method</a> and <b>IStylusPlugin::StylusDown Method</b>.

For example, if you add three packets and your DPP is currently X,Y and Pressure, then you must have nine LONG values in this buffer and set <i>cPropCountPerPkt</i> to 9.

The <i>cPropCountPerPkt</i> value is useful to help clarify the boundaries between packets in the flat array of integers that comes in for events such as the <a href="https://msdn.microsoft.com/2682e7ba-dabd-497e-aea4-6d3f837f4f10">NewPackets Event</a> event. Packets can be bundled in order to be more efficient with data transfer, such that it is not required that a plug-in is called once per packet.


#### Examples

The following C++ code example implements a <b>StylusDown</b> method that calls a helper function, <b>ModifyPacket</b>, to change the value of the X,Y data to make it fall within a specified rectangle. This is the same functionality that is implemented in the C# sample, <a href="https://msdn.microsoft.com/0ba753d1-d81a-4f7a-942c-2967c46febec">RealTimeStylus Plug-in Sample</a>. The second code snippet is the <b>ModifyPacket</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CPacketModifier::StylusDown( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const StylusInfo *pStylusInfo,
            /* [in] */ ULONG cPropCountPerPkt,
            /* [size_is][in] */ LONG *pPacket,
            /* [out][in] */ LONG **ppInOutPkt)
{
	return ModifyPacket(cPropCountPerPkt, pPacket, ppInOutPkt);
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Helper method to modify a single packet
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

	if (cPropCountPerPkt &gt; 0)
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
			x = (x &lt; m_filterRect.left ? m_filterRect.left : x);
			x = (x &gt; m_filterRect.right ? m_filterRect.right : x);
			y = (y &lt; m_filterRect.top ? m_filterRect.top : y);
			y = (y &gt; m_filterRect.bottom ? m_filterRect.bottom : y);

			// If necessary, modify the x,y packet data
			if ((x != pPacket[0]) || (y != pPacket[1]))
			{
				pTempOutPkt[0] = x;
				pTempOutPkt[1] = y;

				// Copy the properties that we haven't modified
				while (iOtherProps &lt; cPropCountPerPkt)
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<b>IStylusPlugin Interface</b>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>
 

 

