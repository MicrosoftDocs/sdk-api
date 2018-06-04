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

# IVssComponent::GetAlternateLocationMappingCount


## -description


The 
<b>GetAlternateLocationMappingCount</b> method returns the number of alternate location mappings used by a requester in restoring data. Either a writer or a requester can call this method.


## -parameters




### -param pcMappings [out]

The address of a caller-allocated variable that receives the number of alternate location mappings.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
</table>
 




## -remarks



The count of alternate location mappings returned by 
<b>GetAlternateLocationMappingCount</b> may be due to not only files in the current component but to files in any of its nonselectable subcomponents.

An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.

The count returned by 
<b>GetAlternateLocationMappingCount</b> refers to the number of alternate location mappings used in the course of restoring files.

The count is updated by calls to 
<a href="https://msdn.microsoft.com/349ec124-f3f5-4142-8600-8d9f508c9bb2">IVssBackupComponents::AddAlternativeLocationMapping</a>.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/8c6537eb-67ba-4d6a-ac86-44da176ef5c5">IVssComponent::GetAlternateLocationMapping</a>
 

 

