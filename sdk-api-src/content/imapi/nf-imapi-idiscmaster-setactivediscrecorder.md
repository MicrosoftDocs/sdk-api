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

# IDiscMaster::SetActiveDiscRecorder


## -description


Selects an active disc recorder. The active disc recorder is the recorder where a burn will occur when 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">RecordDisc</a> is called.


## -parameters




### -param pRecorder [in]

Pointer to the 
<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a> interface of a disc recorder object. This pointer should have been returned by a previous call to 
<a href="https://msdn.microsoft.com/03daab81-11cf-4100-ab5e-3442a5972912">EnumDiscRecorders</a>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



<b>SetActiveDiscRecorder</b> must be called after the media to be used has been inserted, and before calling 
<a href="https://msdn.microsoft.com/91517103-71c5-450c-9d93-584f94cd2c45">IJolietDiscMaster::AddData</a>.

Selecting a recorder while in an active Joliet format will cause IMAPI to read information from the currently installed recorder disc. If this disc is a previous IMAPI Joliet disc and has space for another session, IMAPI automatically sets itself to multi-session mode. This disc must be in the active recorder when 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">RecordDisc</a> is called.

The <b>MaxWriteSpeed</b> property is updated when this method is called. The default setting is the highest write speed.




## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 

