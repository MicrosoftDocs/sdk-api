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

# ISCluster::get_Resources


## -description


<p class="CCE_Message">[The <b>Resources</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns a 
    <a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a> collection providing access 
    to the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a> collection returned 
    by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a> object's 
    <b>Resources</b> property provides access to all the 
    resources in the cluster. To retrieve information about all of the resources owned by a particular 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>, use the 
    <a href="https://msdn.microsoft.com/891a2126-774d-43c6-bd27-6a0e9d943383">ClusResGroup.Resources</a> property.




## -see-also




<a href="https://msdn.microsoft.com/891a2126-774d-43c6-bd27-6a0e9d943383">ClusResGroup.Resources</a>



<a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>
 

 

