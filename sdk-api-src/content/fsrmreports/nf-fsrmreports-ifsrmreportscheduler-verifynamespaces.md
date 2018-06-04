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

# IFsrmReportScheduler::VerifyNamespaces


## -description


<p class="CCE_Message">[Starting with Windows Server 2012 this method is not supported; use the 
    <a href="https://msdn.microsoft.com/8ed0ec1c-3af2-4c49-92cf-0911473fb33a">MSFT_FSRMScheduledTask</a> WMI class to manage 
    scheduled tasks.]

Verifies that the specified local directory paths that are used as the source for the reports are 
    valid.


## -parameters




### -param namespacesSafeArray [in]

A <b>VARIANT</b> that contains a <b>SAFEARRAY</b> of local 
      directory paths. Each element of the array is a variant of type <b>VT_BSTR</b>. Use the 
      <b>bstrVal</b> member of the variant to set the path.


## -returns



The method returns the following return values.




## -remarks



If the paths are valid, you can use them when calling the 
    <a href="https://msdn.microsoft.com/983a6d05-417f-4aea-9652-955fd96e78f0">IFsrmReportScheduler::CreateScheduleTask</a> 
    method.

The paths are valid if:

<ul>
<li>All paths in the array are on NTFS volumes.</li>
<li>All paths in the array are on volumes that are online accessible.</li>
<li>For clusters, all paths are on volumes that are in the same failover group.</li>
</ul>
If one of the paths fails to validate, there is no indication of which path failed. To determine which path 
    failed, you need to call this method for each path separately. For clusters, if all paths validate, you need to 
    verify the cluster groups using the cluster APIs.




## -see-also




<a href="https://msdn.microsoft.com/306f1d7f-6ad4-457a-97be-193aefeccfeb">FsrmReportScheduler</a>



<a href="https://msdn.microsoft.com/f3e71a39-d880-4035-a719-42ace5eeb9e0">IFsrmReportScheduler</a>
 

 

