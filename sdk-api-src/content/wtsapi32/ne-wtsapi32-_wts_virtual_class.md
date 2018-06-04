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

# _WTS_VIRTUAL_CLASS enumeration


## -description


Contains values that indicate the type of virtual channel information to retrieve.


## -enum-fields




### -field WTSVirtualClientData

This value is not currently supported.


### -field WTSVirtualFileHandle

Indicates a request for the file handle of a virtual channel that can be used for asynchronous I/O.


## -remarks



For an example that shows the use of the WTSVirtualFileHandle value, see <a href="https://msdn.microsoft.com/68ae8174-d72b-4b1c-b8e9-ae5fed51d385">WTSVirtualChannelQuery</a>. This example shows how to gain access to a virtual channel file handle that can be used for asynchronous I/O.




## -see-also




<a href="https://msdn.microsoft.com/68ae8174-d72b-4b1c-b8e9-ae5fed51d385">WTSVirtualChannelQuery</a>
 

 

