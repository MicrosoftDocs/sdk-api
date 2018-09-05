---
UID: NE:vswriter.VSS_COMPONENT_TYPE
title: VSS_COMPONENT_TYPE
author: windows-sdk-content
description: Specify the type of component being used with a shadow copy backup operation.
old-location: base\vss_component_type.htm
old-project: VSS
ms.assetid: ba3b726c-448a-46c0-8fa5-5793497aa385
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: VSS_COMPONENT_TYPE, VSS_COMPONENT_TYPE enumeration [VSS], VSS_CT_DATABASE, VSS_CT_FILEGROUP, VSS_CT_UNDEFINED, _win32_vss_component_type, base.vss_component_type, enumeration [VSS], vswriter/VSS_COMPONENT_TYPE, vswriter/VSS_CT_DATABASE, vswriter/VSS_CT_FILEGROUP, vswriter/VSS_CT_UNDEFINED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vswriter.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VSS_COMPONENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsWriter.h
api_name:
 - VSS_COMPONENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

