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

# IFaxIncomingJob::get_JobType


## -description


Retrieves the <b>JobType</b> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <a href="https://msdn.microsoft.com/53768e23-f93c-4fa7-b16e-23292f5a4380">JobType</a> property describes the type of fax job; for example, the job can be a receive job, a send job, or a routing job.


## -parameters




### -param pJobType [out, retval]

Type: <b><a href="https://msdn.microsoft.com/795b64ce-d2bb-4b33-bf69-4e78c873ffb2">FAX_JOB_TYPE_ENUM</a>*</b>

Pointer to a value from the <a href="https://msdn.microsoft.com/795b64ce-d2bb-4b33-bf69-4e78c873ffb2">FAX_JOB_TYPE_ENUM</a> enumeration that specifies the fax job type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>



<a href="https://msdn.microsoft.com/53768e23-f93c-4fa7-b16e-23292f5a4380">JobType</a>



<a href="https://msdn.microsoft.com/88cde2d4-09ee-4fbf-8a75-35de58dd45f5">Visual Basic Example</a>
 

 

