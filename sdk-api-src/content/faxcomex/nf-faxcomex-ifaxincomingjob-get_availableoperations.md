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

# IFaxIncomingJob::get_AvailableOperations


## -description


Retrieves the <b>AvailableOperations</b> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <b>AvailableOperations</b> property indicates the combination of valid operations that you can perform on the fax job given its current status.


## -parameters




### -param pAvailableOperations






#### - plAvailableOperations [out, retval]

Type: <b><a href="https://msdn.microsoft.com/557655b9-d59b-4255-b071-4c1fbec3a889">FAX_JOB_OPERATIONS_ENUM</a>*</b>

Pointer to a <b>long</b> value from the <a href="https://msdn.microsoft.com/557655b9-d59b-4255-b071-4c1fbec3a889">FAX_JOB_OPERATIONS_ENUM</a> enumeration that specifies a bitwise combination of the operations that you can currently perform on the fax job. Some operations are mutually exclusive. For example, you cannot pause a job that has already been paused. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/04149d5c-e26f-4cef-9ae0-eba2a199ec51">AvailableOperations</a>



<a href="https://msdn.microsoft.com/557655b9-d59b-4255-b071-4c1fbec3a889">FAX_JOB_OPERATIONS_ENUM</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>
 

 

