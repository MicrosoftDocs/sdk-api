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

# _PEERDIST_CLIENT_BASIC_INFO structure


## -description


The <b>PEERDIST_CLIENT_BASIC_INFO</b> structure indicates whether or not there are many clients simultaneously downloading the same content.


## -struct-fields




### -field fFlashCrowd

Indicates that a "flash crowd" situation has been detected, where many clients in the branch office are simultaneously downloading the same content.  


## -remarks



Thie <b>PEERDIST_CLIENT_BASIC_INFO</b> structure is retrieved from the <a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationHandle</a> function with PeerDistClientBasicInfo value specified for the <i>PeerDistClientInfoClass</i> parameter.

If true,  content that cannot be retrieved from the Peer Distribution APIs may soon be available for retrieval.




## -see-also




<a href="https://msdn.microsoft.com/d3bb080c-cde7-4623-95fd-3cffb3bd93aa">PeerDistClientGetInformationHandle</a>
 

 

