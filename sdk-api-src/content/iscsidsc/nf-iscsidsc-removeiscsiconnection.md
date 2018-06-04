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

# RemoveIScsiConnection function


## -description


The <b>RemoveIscsiConnection</b> function removes a connection from an active session.



## -parameters




### -param UniqueSessionId [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a> that specifies the unique session identifier of the session that the connection belongs to.


### -param ConnectionId

TBD




#### - UniqueConnectionId [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/cc68fda4-6dbf-42de-8e0e-e144bd4e9524">ISCSI_UNIQUE_CONNECTION_ID</a> that specifies the connection to remove. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



The <b>RemoveIscsiConnection</b> function will not remove the last connection of a session or the leading connection of a session. The caller must close the session by calling <a href="https://msdn.microsoft.com/c49ad2e2-3f06-48e7-bf38-6074f9a6bcad">LogoutIscsiTarget</a> to remove the last connection.






## -see-also




<a href="https://msdn.microsoft.com/c49ad2e2-3f06-48e7-bf38-6074f9a6bcad">LogoutIscsiTarget</a>
 

 

