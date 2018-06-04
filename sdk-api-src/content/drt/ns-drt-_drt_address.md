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

# _DRT_ADDRESS structure


## -description


The <b>DRT_ADDRESS</b> structure contains endpoint information about a DRT node that participated in a search.  This information is intended for use in debugging connectivity problems.


## -struct-fields




### -field socketAddress

Contains the endpoint on which the DRT protocol is listening on the remote node.


### -field flags

Holds information explaining how this node behaved in the key lookup.


### -field nearness

Contains the number of bits that the key published by this node shares in common with the target key in the search.


### -field latency

Round trip time to this node.


## -see-also




<a href="https://msdn.microsoft.com/a795dff7-4182-42ad-b14b-142a6c1312c7">DRT_ADDRESS_LIST</a>
 

 

