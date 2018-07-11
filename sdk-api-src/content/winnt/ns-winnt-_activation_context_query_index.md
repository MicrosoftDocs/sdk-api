---
UID: NS:winnt._ACTIVATION_CONTEXT_QUERY_INDEX
title: "_ACTIVATION_CONTEXT_QUERY_INDEX"
author: windows-sdk-content
description: The ACTIVATION_CONTEXT_QUERY_INDEX structure is used by QueryActCtxW function.
old-location: setup\activation_context_query_index.htm
old-project: sbscs
ms.assetid: eb15895c-07c9-4b68-83ef-2f2b8e3b271c
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PACTIVATION_CONTEXT_QUERY_INDEX, ACTIVATION_CONTEXT_QUERY_INDEX, ACTIVATION_CONTEXT_QUERY_INDEX structure [Side-by-side Assemblies], PACTIVATION_CONTEXT_QUERY_INDEX, PACTIVATION_CONTEXT_QUERY_INDEX structure pointer [Side-by-side Assemblies], _ACTIVATION_CONTEXT_QUERY_INDEX, _win32_activation_context_query_index, setup.activation_context_query_index, winnt/ACTIVATION_CONTEXT_QUERY_INDEX, winnt/PACTIVATION_CONTEXT_QUERY_INDEX"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: ACTIVATION_CONTEXT_QUERY_INDEX, *PACTIVATION_CONTEXT_QUERY_INDEX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACTIVATION_CONTEXT_QUERY_INDEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



