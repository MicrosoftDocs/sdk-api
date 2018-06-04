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

# ISCluster::put_QuorumResource


## -description


<p class="CCE_Message">[The <b>QuorumResource</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the 
    current <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a> for a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> or allows a new quorum resource to be 
    designated.

This property is read/write.


## -parameters


## -remarks



An alternate way to assign a quorum resource is to call that resource's 
    <a href="https://msdn.microsoft.com/fd316586-8553-4c4a-824e-ee5b7bf48184">ClusResource.BecomeQuorumResource</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>



<a href="https://msdn.microsoft.com/fd316586-8553-4c4a-824e-ee5b7bf48184">ClusResource.BecomeQuorumResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>
 

 

