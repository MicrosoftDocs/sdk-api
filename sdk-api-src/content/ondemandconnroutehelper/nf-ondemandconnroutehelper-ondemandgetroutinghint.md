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

# OnDemandGetRoutingHint function


## -description


The <b>OnDemandGetRoutingHint</b> function looks up a destination in the Route Request cache and, if a match is found, return the corresponding Interface ID.


## -parameters




### -param destinationHostName

TBD


### -param interfaceIndex

TBD




#### - DestinationHostName [in]

An PWSTR describing the target host name for a network communication.


#### - pInterfaceIndex [out]

The interface index of the network adapter to be used for communicating with the target host.


## -returns



This function returns the following to indicate operation results:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
A match was found in the dll cache. The <i>pdwInterfaceIndex</i> will contain the index of the interface to be used to communicate with the target host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
A match was not found in the dll cache for the specified host name.

</td>
</tr>
</table>
 



