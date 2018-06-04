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

# ReportIScsiSendTargetPortalsExW function


## -description


The <b>ReportIscsiSendTargetPortalsEx</b> function  retrieves a list of static target portals that the iSCSI initiator service uses to perform automatic discovery with <b>SendTarget</b> requests.


## -parameters




### -param PortalCount [out]

A pointer to a location that, on input, contains the number of entries in the <i>PortalInfo</i> array. On output, this parameter specifies the number of elements that contain return data. 


### -param PortalInfoSize [in, out]

A pointer to a location that, on input, contains the byte-size of the buffer specified by <i>PortalInfo</i>. On output, this parameter specifies the number of bytes retrieved. 


### -param PortalInfo [in, out]

Pointer to an array of elements contained in a <a href="https://msdn.microsoft.com/3592b289-9c0d-43dc-918f-23c8ff079186">ISCSI_TARGET_PORTAL_INFO_EX</a> structure that describe the portals that the iSCSI initiator service utilizes to perform discovery with <b>SendTargets</b> requests. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the size of the buffer at <i>PortalInfo</i> is insufficient to contain the output data. Otherwise, <b>ReportIscsiSendTargetPortalsEx</b> returns the appropriate Win32 or iSCSI error code on failure.





## -see-also




<a href="https://msdn.microsoft.com/3592b289-9c0d-43dc-918f-23c8ff079186">ISCSI_TARGET_PORTAL_INFO_EX</a>
 

 

