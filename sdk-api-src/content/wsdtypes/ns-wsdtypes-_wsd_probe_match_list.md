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

# _WSD_PROBE_MATCH_LIST structure


## -description


Represents a node in a single-linked list of ProbeMatch message structures.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSD_PROBE_MATCH_LIST</b> structures.


### -field Element

Reference to a <a href="https://msdn.microsoft.com/a30b11c8-df26-495d-87c3-aa67e400ec28">WSD_PROBE_MATCH</a> structure that contains the ProbeMatch message referenced by this node.


## -see-also




<a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe Message</a>



<a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatches Message</a>



<a href="https://msdn.microsoft.com/f84f7e77-ffe2-41af-a10f-a626466e9847">WSD_PROBE</a>



<a href="https://msdn.microsoft.com/a30b11c8-df26-495d-87c3-aa67e400ec28">WSD_PROBE_MATCH</a>



<a href="https://msdn.microsoft.com/41bf8dc2-903a-43d4-b63d-a34242d47288">WSD_PROBE_MATCHES</a>
 

 

