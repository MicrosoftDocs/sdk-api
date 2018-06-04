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

# VSS_COMPONENT_TYPE enumeration


## -description


The <b>VSS_COMPONENT_TYPE</b> enumeration is used by both 
    the requester and the writer to specify the type of component being used with a shadow copy backup 
    operation.


## -enum-fields




### -field VSS_CT_UNDEFINED

Undefined component type. 
      

This value indicates an application error.


### -field VSS_CT_DATABASE

Database component.


### -field VSS_CT_FILEGROUP

File group component. This is any component other than a database.


## -remarks



A writer sets a component's type when it adds the component to its Writer Metadata Document using 
    <a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a>.

Writers and requesters can find the type information of components selected for inclusion in a Backup 
    Components Document through calls to 
    <a href="https://msdn.microsoft.com/89675df6-dcfd-4167-aa6f-5c88e619ef1c">IVssComponent::GetComponentType</a> to return 
    a component type directly.

A requester can obtain the type of any component in a given writer's Writer Metadata Document by doing the 
    following:

<ol>
<li>Using 
      <a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a> 
      to obtain a <a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a> interface</li>
<li>Using 
      <a href="https://msdn.microsoft.com/ac01bfea-e60f-4f50-a865-5bb7e372fbf2">IVssWMComponent::GetComponentInfo</a> to 
      return a <a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a> structure</li>
<li>Examining the <b>Type</b> member of the 
      <a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a> object</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/89675df6-dcfd-4167-aa6f-5c88e619ef1c">IVssComponent::GetComponentType</a>



<a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a>



<a href="https://msdn.microsoft.com/cb89c3cc-5a8e-419e-839c-f72a1886eadf">VSS_SOURCE_TYPE</a>
 

 

