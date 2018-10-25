---
UID: NF:rtscom.IRealTimeStylus.GetDesiredPacketDescription
title: IRealTimeStylus::GetDesiredPacketDescription
author: windows-sdk-content
description: Retrieves the list of properties that have been requested to be included in the packet stream.
old-location: tablet\irealtimestylus_getdesiredpacketdescription.htm
tech.root: tablet
ms.assetid: 8799eb17-8ad0-49c1-a278-40b3bff9d281
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 8799eb17-8ad0-49c1-a278-40b3bff9d281, GetDesiredPacketDescription, GetDesiredPacketDescription method [Tablet PC], GetDesiredPacketDescription method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],GetDesiredPacketDescription method, IRealTimeStylus.GetDesiredPacketDescription, IRealTimeStylus::GetDesiredPacketDescription, rtscom/IRealTimeStylus::GetDesiredPacketDescription, tablet.irealtimestylus_getdesiredpacketdescription
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
 - IRealTimeStylus.GetDesiredPacketDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRealTimeStylus::GetDesiredPacketDescription


## -description


Retrieves the list of properties that have been requested to be included in the packet stream.
        


## -parameters




### -param pcProperties [in, out]

The size, in bytes, of the <i>ppPropertyGUIDS</i> buffer.


### -param ppPropertyGuids [out]

 A pointer to a list of GUIDs specifying which properties, such as X, Y, and NormalPressure, are present in the packet data. For a list of predefined properties, see <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Use this method to get the array of packet properties to which the <a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a> object has subscribed by calling <a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>. The packet properties are represented by an array of globally unique identifiers (GUIDs). For a complete list of properties for which you can retrieve metrics, see the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>.

The default is an array of GUIDs that contains the X, Y and normal pressure GUIDs.

The <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> uses <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> to allocate space for the GUIDs. The caller should call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when the array is no longer needed.

If called on a child <a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a> object (cascading configuration) and connected, this method returns the parent's packet description if connected, otherwise this method returns the default (X, Y, pressure) or whatever properties were set in an earlier call to the <a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>.

The following list describes how the <a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a> object orders the packet property GUIDs.

<ul>
<li>By default, the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method returns GUID_X, GUID_Y, and GUID_NORMAL_PRESSURE.</li>
<li>The X and Y GUIDs are always returned in the first two positions in the array by the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method, whether they were specified in a previous call to the <a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a> method.</li>
<li>If GUID_PACKET_STATUS is specified in the call to the <a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a> method, GUID_PACKET_STATUS is always returned in the last position in the array by the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method.</li>
<li>If any GUIDs are specified more than once in the call to the <a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a> method, each GUID occurs only once in the array returned by the <b>IRealTimeStylus::GetDesiredPacketDescription Method</b> method.</li>
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




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<b>RealTimeStylus Class</b>
 

 

