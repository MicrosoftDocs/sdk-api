---
UID: NF:vsprov.IVssHardwareSnapshotProvider.OnLunEmpty
title: IVssHardwareSnapshotProvider::OnLunEmpty
author: windows-sdk-content
description: Called whenever VSS determines that a shadow copy LUN contains no interesting data.
old-location: base\ivsshardwaresnapshotprovider_onlunempty.htm
old-project: VSS
ms.assetid: 06a31704-9031-4ab9-84eb-685f6b648d27
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssHardwareSnapshotProvider interface [VSS],OnLunEmpty method, IVssHardwareSnapshotProvider.OnLunEmpty, IVssHardwareSnapshotProvider::OnLunEmpty, OnLunEmpty, OnLunEmpty method [VSS], OnLunEmpty method [VSS],IVssHardwareSnapshotProvider interface, base.ivsshardwaresnapshotprovider_onlunempty, vsprov/IVssHardwareSnapshotProvider::OnLunEmpty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: VSS_MGMT_OBJECT_UNION, *PVSS_MGMT_OBJECT_UNION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VsProv.h
api_name:
-	IVssHardwareSnapshotProvider.OnLunEmpty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssHardwareSnapshotProvider::OnLunEmpty


## -description



		 The <b>OnLunEmpty</b> method is 
   called whenever VSS determines that a shadow copy LUN contains no interesting data. All 
   shadow copies have been deleted (which also causes deletion of the LUN.) The LUN resources may be reclaimed by the 
   provider and reused for another purpose. VSS will dismount any affected volumes. A provider should not issue a 
   rescan during  <b>OnLunEmpty</b>. VSS 
   will handle this cleanup.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters




### -param wszDeviceName [in]

Device corresponding to the LUN that contains the shadow copy to be deleted.


### -param pInformation [in]

Pointer to a <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure 
      containing information about the LUN containing the shadow copy to be deleted.


## -returns



This method can return one of these values.

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
An unexpected provider error occurred. The provider must report an event in the application event log 
        providing the user with information on how to resolve the problem.

</td>
</tr>
</table>
 




## -remarks



Hardware providers should delete a shadow copy and reclaim the LUN if and only if  
    <b>OnLunEmpty</b> is being called. A 
    hardware shadow copy may be used as the backup media itself, therefore the LUNs should be treated with the same 
    care the storage array treats LUNs used for regular disks. Reclaiming LUNs outside of processing for 
    <b>OnLunEmpty</b> should be limited to 
    emergency or an administrator performing explicit action manually.

In the case of persistent shadow copies, the requester deletes the shadow copy when it is no longer needed. In the case of 
    nonpersistent auto-release shadow copies, the VSS service deletes the shadow copy when the requester calls <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on the <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> object. In the case of nonpersistent non-auto-release shadow copies, the VSS service deletes the shadow copy when the computer is restarted. In all cases, the VSS service calls the provider's  <b>OnLunEmpty</b> method as needed for each shadow copy 
    LUN.

Note that <b>OnLunEmpty</b> is 
    called on a best effort basis. VSS invokes the method only when the LUN is guaranteed to be empty. There may be 
    many cases where the LUN is empty but VSS is unable to detect this due to errors or external circumstances. In 
    this case, the user should use storage management software to clear this state.

Some examples:

<ul>
<li>When a shadow copy LUN is moved to a different host but not actually transported or imported through VSS, 
      then that LUN appears as any other LUN, and volumes can be simply deleted without any  notification of VSS.</li>
<li>A crash or unexpected reboot in the middle of a shadow copy creation.</li>
<li>A canceled import.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/97fbb6bf-110e-4393-bf25-1ec378b91bdc">IVssHardwareSnapshotProvider</a>
 

 

