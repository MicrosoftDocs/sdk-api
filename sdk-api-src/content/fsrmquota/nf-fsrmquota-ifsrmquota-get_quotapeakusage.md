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

# IFsrmQuota::get_QuotaPeakUsage


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the highest amount of disk space usage charged to this quota.

This property is read-only.


## -parameters


## -remarks



The value represents the highest amount of disk space charged to this quota since the last call to 
    <a href="https://msdn.microsoft.com/5c2b18a9-912a-49cc-bf4f-07f172a328b1">IFsrmQuota::ResetPeakUsage</a>. To reset this value, 
    call the <b>ResetPeakUsage</b> method.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/7b755410-5520-4933-8859-9c201cbd13eb">Getting Current Usage Values</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

