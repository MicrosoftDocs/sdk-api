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

# ITfCompartmentEventSink::OnChange


## -description




## -parameters




### -param rguid [in]

Contains a GUID that identifies the compartment that changed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When this method is called, the data has changed. The new data can be obtained at this time by calling <a href="https://msdn.microsoft.com/31a9efbd-ebde-4877-a387-ebaccd97d732">ITfCompartment::GetValue</a>.


<a href="https://msdn.microsoft.com/1a1a175f-a24e-4f83-92d3-ac6a24f5f486">ITfCompartment::SetValue
        </a> will return E_UNEXPECTED if called from within this notification.




## -see-also




<a href="https://msdn.microsoft.com/31a9efbd-ebde-4877-a387-ebaccd97d732">ITfCompartment::GetValue
      </a>



<a href="https://msdn.microsoft.com/1a1a175f-a24e-4f83-92d3-ac6a24f5f486">
        ITfCompartment::SetValue
      </a>



<a href="https://msdn.microsoft.com/1bd464e7-9e34-4725-83f9-42e09ddf4778">ITfCompartmentEventSink</a>
 

 

