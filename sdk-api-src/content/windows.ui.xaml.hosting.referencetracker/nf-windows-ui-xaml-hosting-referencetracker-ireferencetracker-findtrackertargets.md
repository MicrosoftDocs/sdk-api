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

# IReferenceTracker::xaml


## -description


Finds out what reference tracker targets are reachable from a reference tracker source; must be called by a garbage collector between calls to <a href="https://msdn.microsoft.com/8d911bbb-aa5e-4906-86d6-caf6f3f84f6f">ReferenceTrackingStarted</a> and <a href="https://msdn.microsoft.com/16e6f9ac-0466-4ada-ad72-278b3dba6a26">FindTrackerTargetsCompleted</a>.  


## -parameters




### -param callback [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2267d29f-c3b2-4bc8-b4cb-6272a7ebae1a">IReferenceTracker</a>
 

 

