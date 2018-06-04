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

# IReferenceTrackerManager::xaml


## -description


Indicates that a garbage collector is performing a collection; when the collection is finished, the garbage collector calls <a href="https://msdn.microsoft.com/16e6f9ac-0466-4ada-ad72-278b3dba6a26">FindTrackerTargetsCompleted</a>.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



  When this method is called, XAML blocks all threads where it is attempting to update tracked references.  Between calls to <b>ReferenceTrackingStarted</b> and <a href="https://msdn.microsoft.com/17f3832f-c3cb-4797-8f48-c1cf0c9e408a">ReferenceTrackingCompleted</a>, XAML does not make any calls to reference tracker target objects other than <a href="https://msdn.microsoft.com/2750e8b1-eeeb-411a-89a8-b63b26f731ac">Peg</a> and <a href="https://msdn.microsoft.com/c070957f-3bf8-4e72-ad56-e9cb023692c6">Unpeg</a>.




## -see-also




<a href="https://msdn.microsoft.com/bdac39a0-a51a-49cc-b554-58450c722a46">IReferenceTrackerManager</a>
 

 

