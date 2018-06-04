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

# SetupPersistentIScsiDevices function


## -description


The <b>SetupPersistentIscsiDevices</b> function builds the list of devices and volumes assigned to iSCSI targets that are connected to the computer, and saves this list in non-volatile cache of the iSCSI initiator service.



## -parameters






## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



When the iSCSI Initiator service starts, it does not complete initialization until the storage stack can access and enumerate all persistent iSCSI volumes and devices. If there is a service that is dependent on data stored on a persistent volume or device, it should be configured to have a dependency on the iSCSI service (MSiSCSI).

The correct procedure for a system administrator to configure a computer to use external persistent volumes is as follows:

 

 


 



<ul>
<li>Login to all of the targets that contain the volumes</li>
<li>Configure all volumes on top of the disks</li>
<li>Use management software to call the <b>SetupPersistentIscsiDevices</b> routine, so that the iSCSI initiator service will add the volumes to its list of persistent volumes.</li>
</ul>


