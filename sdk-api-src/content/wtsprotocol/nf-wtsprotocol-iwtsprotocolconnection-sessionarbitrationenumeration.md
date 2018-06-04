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

# IWTSProtocolConnection::SessionArbitrationEnumeration


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::SessionArbitrationEnumeration</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/d0e93014-1f79-47ac-bf3a-c100eb652751">IWRdsProtocolConnection::SessionArbitrationEnumeration</a>.]

Retrieves a collection of session IDs for reconnection.


## -parameters




### -param hUserToken [in]

A pointer to a user token handle.


### -param bSingleSessionPerUserEnabled [in]

A Boolean value that specifies whether a user can be associated with, at most, one session.


### -param pSessionIdArray [out]

A pointer to an array of integers that contains the disconnected session IDs for the user.


### -param pdwSessionIdentifierCount [in, out]

A pointer to an integer that specifies the number of disconnected session IDs referenced by  the <i>pSessionIdArray</i> parameter.


## -remarks



The Remote Desktop Services service calls this method to find existing sessions that this user can reconnect to. If this method returns an <b>HRESULT</b> error code or it does not return any session IDs,  the Remote Desktop Services service performs arbitration itself.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

