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

# FIND_BY_SID_DATA structure


## -description


Contains data for the 
   <a href="https://msdn.microsoft.com/library/windows/hardware/ff544833">FSCTL_FIND_FILES_BY_SID</a> control 
   code.


## -struct-fields




### -field Restart

Indicates whether to restart the search. This member should be 1 on first call, so the search will start 
      from the root. For subsequent calls, this member should be zero so the search will resume at the point where it 
      stopped.


### -field Sid

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that specifies the desired creator 
      owner.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544833">FSCTL_FIND_FILES_BY_SID</a>
 

 

