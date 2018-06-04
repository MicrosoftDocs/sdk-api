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

# peer_pnrp_endpoint_info_tag structure


## -description


The <b>PEER_PNRP_ENDPOINT_INFO</b> structure contains the IP addresses and data associated with a peer endpoint.


## -struct-fields




### -field pwzPeerName

The peer name associated with this peer endpoint.


### -field cAddresses

The number of SOCKADDR structures in <b>pAddresses</b>.


### -field ppAddresses

Pointer to an array of pointers to SOCKADDR structures that contain the IP addresses for the peer endpoint's network interface.


### -field pwzComment

Pointer to a zero-terminated Unicode string that contains a comment for this peer endpoint.


### -field payload

Pointer to a <a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a> structure that contains application-specific data for the peer endpoint (such as a message or an image).

