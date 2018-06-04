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

# IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots


## -description


The 
   <b>PostFinalCommitSnapshots</b> 
   method supports 
   <a href="vssgloss_a.htm">auto-recover</a> shadow 
   copies. VSS calls this method to notify the provider that the volume will now be read-only until a requester calls <a href="https://msdn.microsoft.com/8c366f19-b10f-46cd-b5dc-cc3c77c5a008">IVssBackupComponents::BreakSnapshotSet</a>.


## -parameters




### -param SnapshotSetId [in]

The <b>VSS_ID</b> that identifies the shadow copy set.


## -returns



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
<dt>0x8007000EL</dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_PROVIDER_VETO</b></b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An unexpected provider error occurred. If this is returned, the error must be described in an entry in 
        the application event log, giving the user information on how to resolve the problem.

</td>
</tr>
</table>
 

If any other value is returned, VSS will write an event to the event log and convert the error to 
      <b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b>.




## -remarks



This method was added in Windows Server 2003 to enable binary compatibility when the 
    <a href="vssgloss_a.htm">auto-recover</a> feature was 
    introduced in Windows Server 2003 with Service Pack 1 (SP1).

<div class="alert"><b>Note</b>  For Windows Server 2003, it is recommended that hardware providers implement this method using 
    the following example:</div>
<div> </div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT PostFinalCommitSnapshots(
    VSS_ID     /* SnapshotSetId */
)
{
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/41a795f0-7882-47a3-9226-aa50218a56e9">IVssProviderCreateSnapshotSet</a>
 

 

