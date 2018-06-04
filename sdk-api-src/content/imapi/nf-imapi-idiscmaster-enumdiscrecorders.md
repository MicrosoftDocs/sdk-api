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

# IDiscMaster::EnumDiscRecorders


## -description


Retrieves an enumerator for all disc recorders supported by the active disc master format.


## -parameters




### -param ppEnum [out]

Address of a pointer to the <b>IEnumDiscRecorders</b> enumerator.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



<b>IEnumDiscRecorders</b> is a standard COM enumerator, as documented in 
<b>IEnumXXXX</b>. Each call to <b>Next</b> returns an array of pointers to 
<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>. Each recorder interface represents a single available recorder already associated with an underlying physical disc recorder.

The list of available recorders may change due to Plug and Play arrivals or departures, or a call to 
<a href="https://msdn.microsoft.com/fcc2840b-d302-4cd6-b576-1826c83b711e">SetActiveDiscMasterFormat</a>. An application is notified of these changes when it receives a call to 
<a href="https://msdn.microsoft.com/d2b41e86-2f1b-46f1-955d-7fc42f8189a4">IDiscMasterProgressEvents::NotifyPnPActivity</a>. When a change occurs, the application should call this method again to retrieve a new enumerator, because each enumerator contains a snapshot of the devices supported at the time of the enumeration.

When a device is removed, its pointer and 
<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a> interface must remain valid even though the underlying physical device is missing. In this case, operations on an 
<b>IDiscRecorder</b> or a request to record a disc may return IMAPI_E_DEVICE_NOTPRESENT.

The <b>MaxWriteSpeed</b> property is updated when this method is called. The default setting is the highest available write speed.




## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 

