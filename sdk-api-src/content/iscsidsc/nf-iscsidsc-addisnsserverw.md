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

# AddISNSServerW function


## -description


The <b>AddIsnsServer</b> function adds a new server to the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service uses to discover targets.


## -parameters




### -param Address [in]

IP address or the DNS name of the server.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. If the operation fails, because of a problem with a socket connection, <b>AddIsnsServer</b> returns a Winsock error code. If the Address parameter does not point to a valid iSNS server name, the <b>AddIsnsServer</b> routine returns ERROR_INVALID_PARAMETER.





## -remarks



When the iSCSI initiator service receives a request from the <b>AddIsnsServer</b> user-mode library function to add an iSNS server, the initiator service saves relevant data about the iSNS server in non-volatile storage. The iSCSI initiator service queries the newly added server for discovered targets immediately after adding it. From that point forward, the iSCSI initiator service automatically queries the iSNS server whenever the initiator service refreshes the target list of the iSNS server. The initiator service also refreshes the target list of the iSNS server at startup or whenever the iSNS server indicates a change.

If management software does not call <b>AddIsnsServer</b> to manually add the new iSNS servers to the service list of the iSCSI initiator service, the initiator service must rely on automatic discovery mechanisms, such as <a href="https://msdn.microsoft.com/d8eb3dde-1a69-4b10-9367-769978b25e45">DHCP</a>, to add new iSNS servers to the list.




## -see-also




<a href="https://msdn.microsoft.com/c954126a-6bad-49cf-889e-81746fe175a4">RefreshIsnsServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563978">RemoveIsnsServer</a>



<a href="https://msdn.microsoft.com/4fa773ac-0d3e-4860-8603-cb36e9278e93">ReportIsnsServerList</a>
 

 

