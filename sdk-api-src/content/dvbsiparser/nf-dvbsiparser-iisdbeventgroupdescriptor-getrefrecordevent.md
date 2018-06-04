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

# IIsdbEventGroupDescriptor::GetRefRecordEvent


## -description


Gets data from a related event record in an Integrated Services Digital Broadcasting (ISDB) event group descriptor. The descriptor contains records for related events if the group_type field of the descriptor has a value of 4 or 5. If this  field has a value of 4, it indicates an event relay to other networks. If this field has a value of 5, it indicates an event movement from other networks.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the related event record containing the data. To get the number of components, call <a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>.


### -param pwOriginalNetworkId [out]

Receives the value of the original_network_id field from the related
event record. This value is transmitted at the time of event relay or event move across networks.


### -param pwTransportStreamId [out]

Receives the value of the transport_stream_id field from the related
event record. This value that is transmitted at the time of event relay or event move across networks.


### -param pwServiceId [out]

Receives the value of the sevice_id field from the related event record. This value identifies the related information service and appears in the program_number field of the corresponding program map section.


### -param pwEventId [out]

Receives the value of  the event_id field from the related event record. This value identifies the related event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1e71f277-0296-4589-8099-dfae2a9dcfb0">IIsdbEventGroupDescriptor</a>



<a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>
 

 

