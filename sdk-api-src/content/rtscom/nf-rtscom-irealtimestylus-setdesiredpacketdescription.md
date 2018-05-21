---
UID: NF:rtscom.IRealTimeStylus.SetDesiredPacketDescription
title: IRealTimeStylus::SetDesiredPacketDescription
author: windows-driver-content
description: Requests properties to be included in the packet stream.
old-location: tablet\irealtimestylus_setdesiredpacketdescription.htm
old-project: tablet
ms.assetid: 1ea8359b-fc9f-4929-9499-c5017eb3d763
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 1ea8359b-fc9f-4929-9499-c5017eb3d763, IRealTimeStylus interface [Tablet PC],SetDesiredPacketDescription method, IRealTimeStylus.SetDesiredPacketDescription, IRealTimeStylus::SetDesiredPacketDescription, SetDesiredPacketDescription, SetDesiredPacketDescription method [Tablet PC], SetDesiredPacketDescription method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::SetDesiredPacketDescription, tablet.irealtimestylus_setdesiredpacketdescription
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
-	IRealTimeStylus.SetDesiredPacketDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRealTimeStylus::SetDesiredPacketDescription


## -description



Requests properties to be included in the packet stream.




## -parameters




### -param cProperties [in]

Count of the properties specified by the <i>pPropertyGuids</i> parameter. Valid values are between 0 and 32, inclusive.


### -param pPropertyGuids [in]

The array of globally unique identifiers (GUIDs) for the properties requested to be included in the packet stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Events receive the actual packet properties in the following order.

<table>
<tr>
<th>Packet order</th>
<th>Description</th>
</tr>
<tr>
<td>
1st position

</td>
<td>
Contains the x-coordinate data for the property regardless of whether X was specified in the <a href="https://msdn.microsoft.com/320cc215-e4e5-4196-8e1b-ca0a30d01d37">DesiredPacketDescription Property</a>.

</td>
</tr>
<tr>
<td>
2nd position

</td>
<td>
Contains the y-coordinate data for the property regardless of whether Y was specified in the <a href="https://msdn.microsoft.com/320cc215-e4e5-4196-8e1b-ca0a30d01d37">DesiredPacketDescription Property</a>.

</td>
</tr>
<tr>
<td>
End position

</td>
<td>
Contains the packet status when packet status is in the <a href="https://msdn.microsoft.com/320cc215-e4e5-4196-8e1b-ca0a30d01d37">DesiredPacketDescription Property</a>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The result of <a href="https://msdn.microsoft.com/7eff81c6-8ed5-434b-8e78-fcdb952f37e8">IRealTimeStylus::GetPacketDescriptionData Method</a> may not match the <b>IRealTimeStylus::SetDesiredPacketDescription Method</b> properties as some of the properties may not be supported by the tablet.</div>
<div> </div>
If the specified packet properties are not supported by the tablet devices, the property data is not returned and is not represented in the packet data array. If the same GUID appears multiple times in the <i>packetDescription</i> argument, only the first appearance is preserved and all following appearances are filtered out. The <b>IRealTimeStylus::SetDesiredPacketDescription Method</b> method can be called only while the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object is disabled.

Attempting to pass in 0 for <i>cProperties</i> and <b>NULL</b> for <i>pPropertyGuids</i> returns E_INVALIDARG.

Calls to the <b>IRealTimeStylus::SetDesiredPacketDescription Method</b> method are immediately reflected in the return value of the <a href="https://msdn.microsoft.com/8799eb17-8ad0-49c1-a278-40b3bff9d281">IRealTimeStylus::GetDesiredPacketDescription Method</a> method.


#### Examples

The following C++ example code sets the properties that are requested to be included in the packet stream.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GUID guidDesiredPacketDescription[] = { GUID_PACKETPROPERTY_GUID_X, 
                                        GUID_PACKETPROPERTY_GUID_Y, 
                                        GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE,
                                        GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE };

// Number of properties in the array
ULONG ulProperties = sizeof(guidDesiredPacketDescription) / sizeof(GUID);

// Set the packet information we'd like to get
if (SUCCEEDED(g_pRealTimeStylus-&gt;SetDesiredPacketDescription(ulProperties, guidDesiredPacketDescription)))
{
    TRACE("Set the desired packet description successfully.\n");
}

GUID* pGuids = NULL;

// See if setting the properties was successful
if (SUCCEEDED(g_pRealTimeStylus-&gt;GetDesiredPacketDescription(&amp;ulProperties, &amp;pGuids)))
{
    TRACE("The RealTimeStylus supports %d properties.\n", ulProperties);

    // Display the values of the GUIDs in debug output
    for (int i = 0; i &lt; ulProperties; i++)
    {
        TRACE("GUID #%d == %d\n", i, pGuids[i]);
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/8799eb17-8ad0-49c1-a278-40b3bff9d281">IRealTimeStylus::GetDesiredPacketDescription Method</a>



<a href="https://msdn.microsoft.com/7eff81c6-8ed5-434b-8e78-fcdb952f37e8">IRealTimeStylus::GetPacketDescriptionData Method</a>



<b>RealTimeStylus Class</b>
 

 

