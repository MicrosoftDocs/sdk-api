---
UID: NS:p2p.peer_data_tag
title: peer_data_tag
author: windows-sdk-content
description: The PEER_DATA structure contains binary data.
old-location: p2p\peer_data.htm
old-project: P2PSdk
ms.assetid: d8a8b9e3-c455-4813-b812-263efe7f5e3e
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_DATA, PEER_DATA, PEER_DATA structure [Peer Networking], PPEER_DATA, PPEER_DATA structure pointer [Peer Networking], p2p.peer_data, p2p/PPEER_DATA, p2p/peer_data_tag, peer_data_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
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
tech.root: 
req.typenames: PEER_DATA, *PPEER_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_data_tag structure


## -description


The <b>PEER_DATA</b> structure contains binary data.


## -struct-fields




### -field cbData

Size of  <b>pbData</b>, in bytes. It is possible for this value to be set to zero if <b>pbData</b> contains no data.


### -field pbData

Pointer to a buffer.


### -field pbData.size_is

 


### -field pbData.size_is.cbData

 




## -see-also




<a href="https://msdn.microsoft.com/93104ca5-b3de-492c-965e-3acd12d05ea6">PEER_EVENT_INCOMING_DATA</a>



<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a>



<a href="https://msdn.microsoft.com/aa340e32-6d7f-4218-b120-8c352fdbda0f">PFNPEER_FREE_SECURITY_DATA</a>



<a href="https://msdn.microsoft.com/454b40f6-a7de-4b59-ae35-a809c4510133">PFNPEER_SECURE_RECORD</a>
 

 

