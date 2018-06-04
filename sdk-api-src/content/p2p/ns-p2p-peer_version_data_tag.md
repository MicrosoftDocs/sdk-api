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

# peer_version_data_tag structure


## -description


The <b>PEER_VERSION_DATA</b> structure contains the version information about the Peer Graphing and Grouping APIs.


## -struct-fields




### -field wVersion

Specifies the version of the Peer Infrastructure for a caller to use. The version to use is based on the Peer Infrastructure DLL installed on a local computer.  A high order-byte specifies the minor version (revision) number.  A low-order byte specifies the major version number.


### -field wHighestVersion

Specifies the highest version of the Peer Infrastructure that the Peer DLL installed on the local computer can support. Typically, this value is the same as <b>wVersion</b>.


## -see-also




<a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a>



<a href="https://msdn.microsoft.com/c07e200d-9578-4367-a0f8-699ae300fc1f">PeerGroupStartup</a>
 

 

