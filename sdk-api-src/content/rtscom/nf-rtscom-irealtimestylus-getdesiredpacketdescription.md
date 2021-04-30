---
UID: NF:rtscom.IRealTimeStylus.GetDesiredPacketDescription
title: IRealTimeStylus::GetDesiredPacketDescription (rtscom.h)
description: Retrieves the list of properties that have been requested to be included in the packet stream.
helpviewer_keywords: ["8799eb17-8ad0-49c1-a278-40b3bff9d281","GetDesiredPacketDescription","GetDesiredPacketDescription method [Tablet PC]","GetDesiredPacketDescription method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","GetDesiredPacketDescription method","IRealTimeStylus.GetDesiredPacketDescription","IRealTimeStylus::GetDesiredPacketDescription","rtscom/IRealTimeStylus::GetDesiredPacketDescription","tablet.irealtimestylus_getdesiredpacketdescription"]
old-location: tablet\irealtimestylus_getdesiredpacketdescription.htm
tech.root: tablet
ms.assetid: 8799eb17-8ad0-49c1-a278-40b3bff9d281
ms.date: 12/05/2018
ms.keywords: 8799eb17-8ad0-49c1-a278-40b3bff9d281, GetDesiredPacketDescription, GetDesiredPacketDescription method [Tablet PC], GetDesiredPacketDescription method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetDesiredPacketDescription method, IRealTimeStylus.GetDesiredPacketDescription, IRealTimeStylus::GetDesiredPacketDescription, rtscom/IRealTimeStylus::GetDesiredPacketDescription, tablet.irealtimestylus_getdesiredpacketdescription
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
 - IRealTimeStylus::GetDesiredPacketDescription
 - rtscom/IRealTimeStylus::GetDesiredPacketDescription
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
 - IRealTimeStylus.GetDesiredPacketDescription
---

# IRealTimeStylus::GetDesiredPacketDescription


## -description

Retrieves the list of properties that have been requested to be included in the packet stream.

## -parameters

### -param pcProperties [in, out]

The size, in bytes, of the <i>ppPropertyGUIDS</i> buffer.

### -param ppPropertyGuids [out]

 A pointer to a list of GUIDs specifying which properties, such as X, Y, and NormalPressure, are present in the packet data. For a list of predefined properties, see <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketPropertyGuids Constants</a>.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Use this method to get the array of packet properties to which the <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a> object has subscribed by calling <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>. The packet properties are represented by an array of globally unique identifiers (GUIDs). For a complete list of properties for which you can retrieve metrics, see the <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketPropertyGuids Constants</a>.

The default is an array of GUIDs that contains the X, Y and normal pressure GUIDs.

The <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> uses <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> to allocate space for the GUIDs. The caller should call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> when the array is no longer needed.

If called on a child <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a> object (cascading configuration) and connected, this method returns the parent's packet description if connected, otherwise this method returns the default (X, Y, pressure) or whatever properties were set in an earlier call to the <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>.

The following list describes how the <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a> object orders the packet property GUIDs.

<ul>
<li>By default, the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method returns GUID_X, GUID_Y, and GUID_NORMAL_PRESSURE.</li>
<li>The X and Y GUIDs are always returned in the first two positions in the array by the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method, whether they were specified in a previous call to the <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a> method.</li>
<li>If GUID_PACKET_STATUS is specified in the call to the <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a> method, GUID_PACKET_STATUS is always returned in the last position in the array by the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method.</li>
<li>If any GUIDs are specified more than once in the call to the <a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a> method, each GUID occurs only once in the array returned by the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method.</li>
</ul>

#### Examples

The following C++ example code gets the list of properties included in the packet stream.


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



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<b>RealTimeStylus Class</b>