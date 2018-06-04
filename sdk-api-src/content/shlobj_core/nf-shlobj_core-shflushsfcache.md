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

# SHFlushSFCache function


## -description


<p class="CCE_Message">[<b>SHFlushSFCache</b> is available for use in the operating 
    systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Flushes the special folder cache.


## -parameters






## -returns



This function does not return a value.




## -remarks



<b>SHFlushSFCache</b> is called when the path to a special 
    folder is changed. This ensures that the updated path stored in the registry is used rather than the cached 
    value.

For more information on special folders, see the <i>Special Folders and CSIDLs</i> section 
    of <a href="https://msdn.microsoft.com/54225481-a147-4d29-a642-24c9b59fc3ac">Getting a Folder's ID</a>.



