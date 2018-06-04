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

# RemoveIScsiStaticTargetW function


## -description


The <b>RemoveIscsiStaticTarget</b> function removes a target from the list of static targets made available to the machine.


## -parameters




### -param TargetName [in]

The name of the iSCSI target to remove from the static list. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.




## -see-also




<a href="https://msdn.microsoft.com/81f5ac9a-debb-4fa3-8ccf-1303cd45f1de">AddIscsiStaticTarget</a>
 

 

