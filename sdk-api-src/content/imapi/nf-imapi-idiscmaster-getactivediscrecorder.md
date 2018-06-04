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

# IDiscMaster::GetActiveDiscRecorder


## -description


Retrieves an interface pointer to the active disc recorder. The active disc recorder is the recorder where a burn will occur when 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">RecordDisc</a> is called.


## -parameters




### -param ppRecorder [out]

Pointer to the 
<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a> interface of the currently selected disc recorder.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



There is no default active disc recorder. An application using this method must specifically select both an active mastering format and an active disc recorder before initiating a burn.

<div class="alert"><b>Note</b>  The active disc recorder can be invalidated by removing the device or changing the active disc mastering format. For example, a USB CD-R device may be disconnected from the machine while the application is still running (the application is alerted to this condition by a call to 
<a href="https://msdn.microsoft.com/d2b41e86-2f1b-46f1-955d-7fc42f8189a4">IDiscMasterProgressEvents::NotifyPnPActivity</a>). In either case, you must select a new active disc recorder.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 

