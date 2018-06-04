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

# AddRadiusServerW function


## -description


The <b>AddRadiusServer</b> function adds a new Remote Authentication Dial-In User Service (RADIUS)  server to the list referenced by the iSCSI initiator service during authentication.


## -parameters




### -param Address [in]

A string that represents the IP address or DNS name associated with the RADIUS server.


## -returns



Returns ERROR_SUCCESS if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code. Other possible error values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The supplied <i>Address</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



When the iSCSI initiator service receives a request from the <b>AddRadiusServer</b> user-mode library function to add a RADIUS server, the initiator service saves data associated with the server in non-volatile storage. This allows the iSCSI initiator service to utilize the RADIUS server to authenticate targets or obtain authentication information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564020">RemoveRadiusServer</a>
 

 

