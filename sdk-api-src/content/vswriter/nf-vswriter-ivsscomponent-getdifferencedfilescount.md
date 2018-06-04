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

# IVssComponent::GetDifferencedFilesCount


## -description


The <b>GetDifferencedFilesCount</b> 
    method returns the number of file specifications in this component (and in any subcomponents of the 
    component set it defines) marked by a writer supporting an incremental backup or restore as differenced 
    files—that is, backup and restores associated with it are to be implemented as if 
    entire files are copied to and from backup media (as opposed to using partial files).


## -parameters




### -param pcDifferencedFiles [out]

The address of a caller-allocated variable that receives the number of differenced file specifications.


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
 




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/33372d10-c947-45de-9ea2-03ba6378179d">IVssComponent::AddDifferencedFilesByLastModifyTime</a>



<a href="https://msdn.microsoft.com/285b2ac7-d09e-4ac5-bf5c-62c510544353">IVssComponent::GetDifferencedFile</a>



<a href="https://msdn.microsoft.com/e9529aad-cf93-4b4c-811c-0ff0b708de6c">Incremental and Differential Backups</a>
 

 

