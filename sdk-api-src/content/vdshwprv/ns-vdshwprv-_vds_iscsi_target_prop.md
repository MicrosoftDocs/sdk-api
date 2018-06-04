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

# _VDS_ISCSI_TARGET_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of an iSCSI target.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> of the target.


### -field pwszIscsiName

A null-terminated, human-readable string that is the iSCSI name of the target.


### -field pwszFriendlyName

A null-terminated, human-readable string that is the friendly name of the target. This corresponds to the 
     iSCSI alias.


### -field bChapEnabled

If <b>TRUE</b>, a CHAP shared secret is required to login to this target.


## -see-also




<a href="https://msdn.microsoft.com/db48ec8e-aae1-4b88-9942-6a23de2cfe25">IVdsIscsiTarget::GetProperties</a>
 

 

