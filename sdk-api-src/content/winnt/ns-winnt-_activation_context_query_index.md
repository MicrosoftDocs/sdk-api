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

# _ACTIVATION_CONTEXT_QUERY_INDEX structure


## -description


The 
<b>ACTIVATION_CONTEXT_QUERY_INDEX</b> structure is used by 
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> function.


## -struct-fields




### -field ulAssemblyIndex

One-based index of the assembly whose file table is to be queried.


### -field ulFileIndexInAssembly

Zero-based index of the file in the above assembly to be queried.


## -remarks



Calling the 
<a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> function with the FileInformationInAssemblyOfAssemblyInActivationContext option requires that the <i>pvSubInstance</i> parameter point to an 
<b>ACTIVATION_CONTEXT_QUERY_INDEX</b> structure. See the sample for 
<a href="https://msdn.microsoft.com/7f1e5155-a6c1-4b6a-be47-37fab337186c">ASSEMBLY_FILE_DETAILED_INFORMATION</a> for an example of its use.



