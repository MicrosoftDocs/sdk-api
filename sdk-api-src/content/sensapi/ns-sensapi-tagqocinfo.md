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

# tagQOCINFO structure


## -description


The 
<b>QOCINFO</b> structure is returned by the 
<a href="https://msdn.microsoft.com/377af331-8494-4a3d-b822-78c2b568239c">IsDestinationReachable</a> function and provides Quality of Connection information to the caller.


## -struct-fields




### -field dwSize

Upon calling 
<a href="https://msdn.microsoft.com/377af331-8494-4a3d-b822-78c2b568239c">IsDestinationReachable</a>, the caller must specify the size of the <b>QOCINFO</b> structure being provided to the function using dwSize. The size should be specified in bytes. Upon return from <a href="https://msdn.microsoft.com/377af331-8494-4a3d-b822-78c2b568239c">IsDestinationReachable</a>, dwSize contains the size of the provided structure in bytes.


### -field dwFlags

Provides information on the type of network connection available. The following table lists the possible values.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETWORK_ALIVE_LAN"></a><a id="network_alive_lan"></a><dl>
<dt><b>NETWORK_ALIVE_LAN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The computer has one or more active LAN cards.

</td>
</tr>
<tr>
<td width="40%"><a id="NETWORK_ALIVE_WAN"></a><a id="network_alive_wan"></a><dl>
<dt><b>NETWORK_ALIVE_WAN</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The computer has one or more active RAS connections.

</td>
</tr>
<tr>
<td width="40%"><a id="NETWORK_ALIVE_AOL"></a><a id="network_alive_aol"></a><dl>
<dt><b>NETWORK_ALIVE_AOL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
This flag is not supported.

</td>
</tr>
</table>
 


### -field dwInSpeed

Speed of data coming in from the destination in bytes per second.


### -field dwOutSpeed

Speed of data sent to the destination in bytes per second.


## -see-also




<a href="https://msdn.microsoft.com/377af331-8494-4a3d-b822-78c2b568239c">IsDestinationReachable</a>
 

 

