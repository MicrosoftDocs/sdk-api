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

# peer_node_info_tag structure


## -description


The <b>PEER_NODE_INFO</b> structure contains information that is specific to a particular node in a peer graph.


## -struct-fields




### -field dwSize

Specifies the size of the data structure. Set the value to   sizeof(<b>PEER_NODE_INFO</b>). This member is required and has no default value.


### -field ullNodeId

Specifies a unique ID that identifies an application's  connection to its neighbor. An application cannot set the value of this member, it is created by the Peer Graphing Infrastructure.


### -field pwzPeerId

Specifies the ID of this peer. This value is set for the application by the Peer Graphing Infrastructure. when the application creates or opens a peer graph.


### -field cAddresses

Specifies the number of addresses in <b>pAddresses</b>. This member is required and has no default value.


### -field pAddresses

Points to  an array of <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structures that indicate which addresses and  ports this instance is listening to for group traffic. This member is required and has no default value.


### -field pwzAttributes

Points to a string  that contains the  attributes that describe this particular node. This string is a free-form text string that is specific to the application. This parameter is optional; the default value is <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/7149aba3-d44b-4492-aa56-4d8dbfba7b7c">PeerGraphGetNodeInfo</a>
 

 

