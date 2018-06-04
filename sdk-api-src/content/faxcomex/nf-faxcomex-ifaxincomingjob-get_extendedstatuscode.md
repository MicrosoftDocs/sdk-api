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

# IFaxIncomingJob::get_ExtendedStatusCode


## -description


Retrieves the <b>ExtendedStatusCode</b> property of a <a href="https://msdn.microsoft.com/ef93899d-e797-4f07-bede-0860b695b32b">FaxIncomingJob</a> object. The <b>ExtendedStatusCode</b> property specifies a code describing the job's extended status.


## -parameters




### -param pExtendedStatusCode [out, retval]

Type: <b><a href="https://msdn.microsoft.com/f0cb862b-cb5c-40bd-9df9-a32f849e45a1">FAX_JOB_EXTENDED_STATUS_ENUM</a>*</b>

Pointer to a value from the <a href="https://msdn.microsoft.com/f0cb862b-cb5c-40bd-9df9-a32f849e45a1">FAX_JOB_EXTENDED_STATUS_ENUM</a> enumeration that specifies the extended job status.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/15333cd3-e71a-451c-ae93-9e217ea0895c">ExtendedStatusCode</a>



<a href="https://msdn.microsoft.com/e3707441-6cdf-4a1c-b408-023a1a597492">IFaxIncomingJob</a>
 

 

