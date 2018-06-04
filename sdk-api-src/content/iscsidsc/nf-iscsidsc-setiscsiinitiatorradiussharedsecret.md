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

# SetIScsiInitiatorRADIUSSharedSecret function


## -description


The <b>SetIscsiInitiatorRADIUSSharedSecret</b> function establishes the Remote Authentication Dial-In User Service (RADIUS) shared secret.


## -parameters




### -param SharedSecretLength [in]

A <b>ULONG</b> value that represents the size, in bytes, of the shared secret contained by the buffer specified by SharedSecret. The shared secret must be at least 22 bytes, and less than, or equal to, 26 bytes in size.



### -param SharedSecret [in]

A string that specifies the buffer containing the shared secret.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.




## -remarks



When an initiator attempts to log in to a target, the initiator can use the RADIUS server for authentication, or to authenticate a target. During this process the initiator uses the <i>SharedSecret</i> to communicate with the RADIUS server.




## -see-also




<a href="https://msdn.microsoft.com/e94e72d2-b93c-41f4-aafc-78e6a97d7a26">LoginIscsiTarget</a>
 

 

