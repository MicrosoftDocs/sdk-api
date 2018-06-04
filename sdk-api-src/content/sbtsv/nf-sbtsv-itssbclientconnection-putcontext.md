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

# ITsSbClientConnection::PutContext


## -description


Can be used by plug-ins to store context information specific to the connection.


## -parameters




### -param contextId [in]

A <b>BSTR</b> variable that contains the context ID. We recommend using unique identifiers as context IDs to avoid collisions between plug-ins. A client connection object can be used by more than one plug-in.  


### -param context [in]

The context information to store.


### -param existingContext [out, optional]

Existing context information for the supplied context ID, if any, is returned in this parameter. The existing information is overwritten. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins can use the client connection object to store context information that is specific to a connection request. This allows plug-ins to remain stateless and rely exclusively on state information stored by connection requests. Plug-ins that use this method can also register for connection request notifications. Contexts can be deleted upon receipt of CONNECTION_REQUEST_FAILED, CONNECTION_REQUEST_TIMEDOUT, or CONNECTION_REQUEST_SUCCEEDED notifications. These notifications indicate that the connection request is about to be deleted.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>
 

 

