---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



You can pass <b>NULL</b> if you do not want the scaling parameters.

The <b>IRealTimeStylus::GetPacketDescriptionData Method</b> uses <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> to allocate space for <i>ppPacketProperties</i>. The caller should call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when the array is no longer needed.

The order of properties in the stream of data sent to plug-ins is the same as the order of the properties returned by <b>IRealTimeStylus::GetPacketDescriptionData Method</b>. Use this method to determine what the hardware is reporting versus what was requested when calling <a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>.


#### Examples

This C++ code example uses the <b>IRealTimeStylus::GetPacketDescriptionData Method</b> method to get information about the ink packet data.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CCustomRenderer::StylusUp( 
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
HRESULT hr = piRtsSrc-&gt;GetAllTabletContextIds(&amp;ulTcidCount, &amp;pTcids);

// Use the first tablet context identifier in the array
tcid = *pTcids;

// Get the packet description data
hr = piRtsSrc-&gt;GetPacketDescriptionData(tcid, &amp;fInkToDeviceScaleX, 
                                        &amp;fInkToDeviceScaleY, &amp;ulPacketProperties,
                                        &amp;pPacketProperties);

// Use the packet description data to do things like scale the ink 
// to the physical display device when rendering your own strokes

	return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/8799eb17-8ad0-49c1-a278-40b3bff9d281">IRealTimeStylus::GetDesiredPacketDescription Method</a>



<a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

