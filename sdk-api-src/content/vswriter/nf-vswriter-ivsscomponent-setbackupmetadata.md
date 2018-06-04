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

# IVssComponent::SetBackupMetadata


## -description



    The 
    <b>SetBackupMetadata</b> method sets backup
    metadata with the component.
   

A writer can call this method only during a backup operation.


    This method cannot be called while handling a 
    <a href="vssgloss_b.htm">BackupComplete</a> (<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>) or 
    <a href="vssgloss_b.htm">BackupShutdown</a> (<a href="https://msdn.microsoft.com/4b6d5efe-703b-4245-81d8-e2fc7f650d4b">CVssWriter::OnBackupShutdown</a>) event.
   


## -parameters




### -param wszData






#### - bstrMetadata [in]

A <b>NULL</b>-terminated wide character string that contains the backup metadata.


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
Successfully set the item.

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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Private metadata has already been written for this component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">

        This method was not called by a writer or, if called by a writer, it either was not called during a backup
        operation or was called while handling a 
        BackupComplete or 
        BackupShutdown event.
       

</td>
</tr>
</table>
 




## -remarks



<b>SetBackupMetadata</b> sets
    private, writer-specific metadata describing a backup operation.
   

The format need not conform to any VSS metadata specification.




## -see-also




<a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a>



<a href="https://msdn.microsoft.com/638b8909-0aef-4066-ade7-4ee6d96b309e">IVssComponent::GetBackupMetadata</a>



<a href="https://msdn.microsoft.com/2b329fa8-21ad-4de9-9857-52e14d51d429">IVssComponent::SetRestoreMetadata</a>
 

 

