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

# _BG_JOB_TIMES structure


## -description


The 
<b>BG_JOB_TIMES</b> structure provides job-related time stamps.


## -struct-fields




### -field CreationTime

Time the job was created. The time is specified as 
<a href="http://go.microsoft.com/fwlink/p/?linkid=128776">FILETIME</a>.


### -field ModificationTime

Time the job was last modified or bytes were transferred. Adding files or calling any of the set methods in the 
<a href="https://msdn.microsoft.com/68909710-f749-487e-b064-9f8630929c53">IBackgroundCopyJob*</a> interfaces changes this value. In addition, changes to the state of the job and calling the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927278">Suspend</a>, 
<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">Resume</a>, 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>, and 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406719">Complete</a> methods change this value. The time is specified as 
<a href="http://go.microsoft.com/fwlink/p/?linkid=128776">FILETIME</a>.


### -field TransferCompletionTime

Time the job entered the BG_JOB_STATE_TRANSFERRED state. The time is specified as 
<a href="http://go.microsoft.com/fwlink/p/?linkid=128776">FILETIME</a>.


## -see-also




<a href="https://msdn.microsoft.com/acc29cc2-b437-4799-9cdb-388a60f117e9">IBackgroundCopyJob::GetTimes</a>
 

 

