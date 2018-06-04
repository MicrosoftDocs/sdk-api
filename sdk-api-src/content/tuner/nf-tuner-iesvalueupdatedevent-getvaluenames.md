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

# IESValueUpdatedEvent::GetValueNames


## -description



      For a name-value pair in the PBDA General Purpose Name-Value Service, gets the name for the value that has been updated. PBDA Media Sink Devices (MSDs) get this name from <b>ValueUpdated</b> events fired by Media Transform Devices (MTDs) that implement the <a href="https://msdn.microsoft.com/6639c483-aebe-43b4-94cd-494b820c1b14">IESValueUpdatedEvent</a> interface.


## -parameters




### -param pbstrNames [out, retval]


            Pointer to a buffer that gets the name that has been updated. The caller is responsible for freeing this memory.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6639c483-aebe-43b4-94cd-494b820c1b14">IESValueUpdatedEvent</a>
 

 

