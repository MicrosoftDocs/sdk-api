---
UID: NF:rtscom.IRealTimeStylus.SetDesiredPacketDescription
title: IRealTimeStylus::SetDesiredPacketDescription (rtscom.h)
description: Requests properties to be included in the packet stream.
helpviewer_keywords: ["1ea8359b-fc9f-4929-9499-c5017eb3d763","IRealTimeStylus interface [Tablet PC]","SetDesiredPacketDescription method","IRealTimeStylus.SetDesiredPacketDescription","IRealTimeStylus::SetDesiredPacketDescription","SetDesiredPacketDescription","SetDesiredPacketDescription method [Tablet PC]","SetDesiredPacketDescription method [Tablet PC]","IRealTimeStylus interface","rtscom/IRealTimeStylus::SetDesiredPacketDescription","tablet.irealtimestylus_setdesiredpacketdescription"]
old-location: tablet\irealtimestylus_setdesiredpacketdescription.htm
tech.root: tablet
ms.assetid: 1ea8359b-fc9f-4929-9499-c5017eb3d763
ms.date: 12/05/2018
ms.keywords: 1ea8359b-fc9f-4929-9499-c5017eb3d763, IRealTimeStylus interface [Tablet PC],SetDesiredPacketDescription method, IRealTimeStylus.SetDesiredPacketDescription, IRealTimeStylus::SetDesiredPacketDescription, SetDesiredPacketDescription, SetDesiredPacketDescription method [Tablet PC], SetDesiredPacketDescription method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::SetDesiredPacketDescription, tablet.irealtimestylus_setdesiredpacketdescription
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
 - IRealTimeStylus::SetDesiredPacketDescription
 - rtscom/IRealTimeStylus::SetDesiredPacketDescription
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
 - IRealTimeStylus.SetDesiredPacketDescription
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

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
Contains the x-coordinate data for the property regardless of whether X was specified in the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription">DesiredPacketDescription Property</a>.

</td>
</tr>
<tr>
<td>
2nd position

</td>
<td>
Contains the y-coordinate data for the property regardless of whether Y was specified in the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription">DesiredPacketDescription Property</a>.

</td>
</tr>
<tr>
<td>
End position

</td>
<td>
Contains the packet status when packet status is in the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription">DesiredPacketDescription Property</a>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The result of <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getpacketdescriptiondata">IRealTimeStylus::GetPacketDescriptionData Method</a> may not match the <b>IRealTimeStylus::SetDesiredPacketDescription Method</b> properties as some of the properties may not be supported by the tablet.</div>
<div> </div>
If the specified packet properties are not supported by the tablet devices, the property data is not returned and is not represented in the packet data array. If the same GUID appears multiple times in the <i>packetDescription</i> argument, only the first appearance is preserved and all following appearances are filtered out. The <b>IRealTimeStylus::SetDesiredPacketDescription Method</b> method can be called only while the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object is disabled.

Attempting to pass in 0 for <i>cProperties</i> and <b>NULL</b> for <i>pPropertyGuids</i> returns E_INVALIDARG.

Calls to the <b>IRealTimeStylus::SetDesiredPacketDescription Method</b> method are immediately reflected in the return value of the <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getdesiredpacketdescription">IRealTimeStylus::GetDesiredPacketDescription Method</a> method.


#### Examples

The following C++ example code sets the properties that are requested to be included in the packet stream.


```cpp
GUID guidDesiredPacketDescription[] = { GUID_PACKETPROPERTY_GUID_X, 
                                        GUID_PACKETPROPERTY_GUID_Y, 
                                        GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE,
                                        GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE };

// Number of properties in the array
ULONG ulProperties = sizeof(guidDesiredPacketDescription) / sizeof(GUID);

// Set the packet information we'd like to get
if (SUCCEEDED(g_pRealTimeStylus->SetDesiredPacketDescription(ulProperties, guidDesiredPacketDescription)))
{
    TRACE("Set the desired packet description successfully.\n");
}

GUID* pGuids = NULL;

// See if setting the properties was successful
if (SUCCEEDED(g_pRealTimeStylus->GetDesiredPacketDescription(&ulProperties, &pGuids)))
{
    TRACE("The RealTimeStylus supports %d properties.\n", ulProperties);

    // Display the values of the GUIDs in debug output
    for (int i = 0; i < ulProperties; i++)
    {
        TRACE("GUID #%d == %d\n", i, pGuids[i]);
    }
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getdesiredpacketdescription">IRealTimeStylus::GetDesiredPacketDescription Method</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-getpacketdescriptiondata">IRealTimeStylus::GetPacketDescriptionData Method</a>



<b>RealTimeStylus Class</b>