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

# _VDS_ISCSI_PORTAL_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of an iSCSI portal.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> of the portal.


### -field address

The IP address and port of the portal.


### -field status


     The status of the portal, enumerated by 
     <a href="https://msdn.microsoft.com/ae39dfb8-6519-4307-8038-3af670553f51">VDS_ISCSI_PORTAL_STATUS</a>.


## -see-also




<a href="https://msdn.microsoft.com/a17597d5-2525-4a0c-acb3-dc69a6ef04ce">IVdsIscsiPortal::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/42e8b161-5e47-4aae-aa23-94b5cacb5698">VDS_IPADDRESS</a>



<a href="https://msdn.microsoft.com/ae39dfb8-6519-4307-8038-3af670553f51">VDS_ISCSI_PORTAL_STATUS</a>
 

 

