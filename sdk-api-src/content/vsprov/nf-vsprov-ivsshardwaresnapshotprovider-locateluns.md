---
UID: NF:vsprov.IVssHardwareSnapshotProvider.LocateLuns
title: IVssHardwareSnapshotProvider::LocateLuns
author: windows-sdk-content
description: Prompts the hardware provider to make the shadow copy LUNs visible to the computer.
old-location: base\ivsshardwaresnapshotprovider_locateluns.htm
tech.root: VSS
ms.assetid: 9a996875-a495-43c1-987e-67c31d0651c7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVssHardwareSnapshotProvider interface [VSS],LocateLuns method, IVssHardwareSnapshotProvider.LocateLuns, IVssHardwareSnapshotProvider::LocateLuns, LocateLuns, LocateLuns method [VSS], LocateLuns method [VSS],IVssHardwareSnapshotProvider interface, base.ivsshardwaresnapshotprovider_locateluns, vsprov/IVssHardwareSnapshotProvider::LocateLuns
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssHardwareSnapshotProvider.LocateLuns
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vsprov.h
: 
- IVssHardwareSnapshotProvider.LocateLuns
: 
---

# IVssHardwareSnapshotProvider::LocateLuns


## -description


The <b>LocateLuns</b> method prompts the hardware provider to make the shadow copy LUNs visible to the computer. The <b>LocateLuns</b> method is called by VSS when a hardware shadow copy set is imported to a computer. 
    The provider is 
   responsible for any unmasking (or "surfacing") at the hardware level.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters




### -param lLunCount [in]

Number of LUNs that contribute to this shadow copy set.


### -param rgSourceLuns [in]

Pointer to an array of <i>iLunCount</i><a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structures, one for each LUN 
      that is part of the shadow copy set to be imported.


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



In the  <i>rgSourceLuns</i> parameter, VSS supplies the same array of <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> 
    structures that the provider previously initialized in its <a href="https://msdn.microsoft.com/299020eb-0afd-41c8-9551-1275eff45fa1">IVssHardwareSnapshotProvider::GetTargetLuns</a> method. For each <b>VDS_LUN_INFORMATION</b> 
    structure in the array, the provider should unmask (or "surface") the corresponding shadow copy LUN to the computer.

Immediately after this method returns, VSS will perform a rescan and enumeration to detect any arrived 
    devices. This causes any exposed LUNs to be discovered by the PnP manager. In parallel with listening for disk arrivals, VSS 
    will also listen for hidden volume arrivals. VSS will stop listening after all volumes that contribute to a shadow copy set 
    appear in the system or a time-out occurs. If some disk or volume devices fail to appear in this window, the 
    requester will be told that only some of the shadow copies were imported by VSS returning 
    <b>VSS_S_SOME_SNAPSHOTS_NOT_IMPORTED</b> to the requester. The requester will also receive the 
    same error from VSS if the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> 
    structures received from the 
    <a href="https://msdn.microsoft.com/299020eb-0afd-41c8-9551-1275eff45fa1">GetTargetLuns</a> and 
    <a href="https://msdn.microsoft.com/4e4e5942-5bc8-4b5e-a651-5bb354514994">IVssHardwareSnapshotProvider::FillInLunInfo</a> methods do not match.

This method cannot be used to map shadow copy LUNs as read-only.




## -see-also




<a href="https://msdn.microsoft.com/f3615770-63a1-49eb-a3b9-b4d349fc33df">AreLunsSupported</a>



<a href="https://msdn.microsoft.com/4e4e5942-5bc8-4b5e-a651-5bb354514994">FillInLunInfo</a>



<a href="https://msdn.microsoft.com/299020eb-0afd-41c8-9551-1275eff45fa1">GetTargetLuns</a>



<a href="https://msdn.microsoft.com/97fbb6bf-110e-4393-bf25-1ec378b91bdc">IVssHardwareSnapshotProvider</a>



<a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>
 

 

