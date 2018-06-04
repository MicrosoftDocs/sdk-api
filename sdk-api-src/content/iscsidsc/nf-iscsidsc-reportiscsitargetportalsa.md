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

# ReportIScsiTargetPortalsA function


## -description


The <b>ReportIscsiTargetPortals</b> function retrieves target portal information discovered by the iSCSI initiator service.


## -parameters




### -param InitiatorName [in, optional]

A string that represents the name of the initiator node.


### -param TargetName [in]

A string that represents the name of the target for which the portal information is retrieved.


### -param TargetPortalTag [in, optional]

A <b>USHORT</b> value that represents a tag associated with the portal.


### -param ElementCount [in, out]

A <b>ULONG</b> value that specifies the number of portals currently reported for the specified target.


### -param Portals [out]

A variable-length array of an <b>ISCSI_TARGET_PORTALW</b> structure. The number of elements contained in this array is specified by the value of <i>ElementCount</i>.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.




## -see-also




<b>ISCSI_TARGET_PORTALW</b>
 

 

