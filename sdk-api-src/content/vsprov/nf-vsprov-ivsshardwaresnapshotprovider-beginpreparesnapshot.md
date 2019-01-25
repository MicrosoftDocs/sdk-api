---
UID: NF:vsprov.IVssHardwareSnapshotProvider.BeginPrepareSnapshot
title: IVssHardwareSnapshotProvider::BeginPrepareSnapshot
author: windows-sdk-content
description: Called for each shadow copy that is added to the shadow copy set.
old-location: base\ivsshardwaresnapshotprovider_beginpreparesnapshot.htm
tech.root: VSS
ms.assetid: 4a8bdffa-bb6e-425d-a708-1f31af302da9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BeginPrepareSnapshot, BeginPrepareSnapshot method [VSS], BeginPrepareSnapshot method [VSS],IVssHardwareSnapshotProvider interface, IVssHardwareSnapshotProvider interface [VSS],BeginPrepareSnapshot method, IVssHardwareSnapshotProvider.BeginPrepareSnapshot, IVssHardwareSnapshotProvider::BeginPrepareSnapshot, base.ivsshardwaresnapshotprovider_beginpreparesnapshot, vsprov/IVssHardwareSnapshotProvider::BeginPrepareSnapshot
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
 - IVssHardwareSnapshotProvider.BeginPrepareSnapshot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssHardwareSnapshotProvider::BeginPrepareSnapshot


## -description


The <b>BeginPrepareSnapshot</b> 
   method is called for each shadow copy that is added to the shadow copy set.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters




### -param SnapshotSetId [in]

Shadow copy set identifier.


### -param SnapshotId [in]

Identifier of the shadow copy to be created.


### -param lContext [in]

Shadow copy context for current shadow copy set as enumerated by 
      <a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>.


### -param lLunCount [in]

Count of LUNs contributing to this shadow copy volume.


### -param rgDeviceNames [in]

Pointer to array of <i>lLunCount</i> pointers to strings, each string containing 
      the name of a LUN to be shadow copied.


### -param rgLunInformation [in, out]

Pointer to array of <i>lLunCount</i><a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structures, one for each LUN 
       contributing to this shadow copy volume.


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
<dt><b><b>VSS_E_MAXIMUM_NUMBER_OF_VOLUMES_REACHED</b></b></dt>
<dt>0x80042312L</dt>
</dl>
</td>
<td width="60%">
The provider has reached the maximum number of volumes it can support.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_NESTED_VOLUME_LIMIT</b></dt>
</dl>
</td>
<td width="60%">
The specified volume is nested too deeply to participate in the VSS operation.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This return code is not supported.

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
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_VOLUME_NOT_SUPPORTED_BY_PROVIDER</b></b></dt>
<dt>0x8004230EL</dt>
</dl>
</td>
<td width="60%">
The provider does not support this volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_UNSUPPORTED_CONTEXT</b></b></dt>
<dt>0x8004231BL</dt>
</dl>
</td>
<td width="60%">
The context specified by <i>lContext</i> is not supported.

</td>
</tr>
</table>
 




## -remarks



This method cannot be called for a virtual hard disk (VHD) that is nested inside another VHD.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>VHDs are not supported.




## -see-also




<a href="https://msdn.microsoft.com/97fbb6bf-110e-4393-bf25-1ec378b91bdc">IVssHardwareSnapshotProvider</a>



<a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>
 

 

