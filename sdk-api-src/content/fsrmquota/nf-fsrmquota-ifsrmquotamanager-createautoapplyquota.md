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

# IFsrmQuotaManager::CreateAutoApplyQuota


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Creates an automatic quota for the specified directory.


## -parameters




### -param quotaTemplateName [in]

The name of a template from which to derive the quota; automatic quotas must derive from a template. The 
      string is limited to 4,000 characters.


### -param path [in]

The local directory path to which the quota applies. The string is limited to 260 characters.


### -param quota [out]

An <a href="https://msdn.microsoft.com/3eb30caa-ce29-4898-b1a7-bd905031ca98">IFsrmAutoApplyQuota</a> interface to the newly 
      created quota object. The specified template is used to initialize the quota. Use this interface to change the 
      quota and to exclude specific subdirectories from the quota. To add the quota to FSRM, call 
      <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmAutoApplyQuota::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



When you save the automatic quota, FSRM creates quotas for all existing subdirectories under the specified 
    directory that do not already contain a quota. When a new subdirectory is created under the specified directory, 
    FSRM uses the properties of the automatic quota to create a quota for the new subdirectory.

If you are creating both the automatic quota and the subdirectories at the same time, you should first 
    create the subdirectories and then create the automatic quota because it provides better performance.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/b4471a75-f8c9-48aa-8ce3-1e998dbe6952">Defining a Quota</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

