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

# IIsdbEventGroupDescriptor::GetRecordEvent


## -description


 Gets data from an event record in an Integrated Services Digital Broadcasting (ISDB) event group descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the event record containing the data. To get the number of components, call <a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>.


### -param pwServiceId [out]

Receives the value of the sevice_id field from the event record. This value identifies the information service and appears in the program_number field of the corresponding program map section. 


### -param pwEventId [out]

Receives the value of  the event_id field from the related event record. This value identifies the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1e71f277-0296-4589-8099-dfae2a9dcfb0">IIsdbEventGroupDescriptor</a>



<a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>
 

 

