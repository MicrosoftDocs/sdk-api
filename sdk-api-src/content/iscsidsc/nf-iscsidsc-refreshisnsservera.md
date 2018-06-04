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

# RefreshISNSServerA function


## -description


The <b>RefreshIsnsServer</b> function instructs the iSCSI initiator service to query the indicated Internet Storage Name Service (iSNS) server to refresh the list of discovered targets for the iSCSI initiator service.



## -parameters




### -param Address [in]

The DNS or IP Address of the iSNS server.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



If the refresh succeeds, the iSCSI initiator service replaces the previous list of targets discovered by the indicated iSNS server with the updated list.

If the iSNS server supports State Change Notifications (SCN), the iSCSI initiator can keep the iSNS target list up to date, without requiring calls of the <b>RefreshIsnsServer</b> function.





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550125">AddIsnsServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563978">RemoveIsnsServer</a>



<a href="https://msdn.microsoft.com/4fa773ac-0d3e-4860-8603-cb36e9278e93">ReportIsnsServerList</a>
 

 

