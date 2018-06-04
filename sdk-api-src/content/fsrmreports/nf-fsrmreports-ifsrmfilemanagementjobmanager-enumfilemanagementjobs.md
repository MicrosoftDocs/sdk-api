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

# IFsrmFileManagementJobManager::EnumFileManagementJobs


## -description


Enumerates the list of existing file management jobs.


## -parameters




### -param options [in]

One or more options to use when enumerating the management jobs. For possible values, see the <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.

<div class="alert"><b>Note</b>  This parameter must be set to either <b>FsrmEnumOptions_IncludeClusterNodes</b> or <b>FsrmEnumOptions_None</b> for this method.</div>
<div> </div>

### -param fileManagementJobs [out]

An <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a> interface that contains a collection of file management jobs.  The variant type of each item in the collection is <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant to get an <a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a> interface to the job.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/f59844ba-2aff-4885-b80b-82f3e1a638d3">FsrmFileManagementJobManager</a>



<a href="https://msdn.microsoft.com/2df0e8d0-1da7-422e-8d02-ad5d030fdd8d">IFsrmFileManagementJobManager</a>



<a href="https://msdn.microsoft.com/106c5237-94bc-4556-aa65-247697133810">IFsrmFileManagementJobManager::GetFileManagementJob</a>
 

 

