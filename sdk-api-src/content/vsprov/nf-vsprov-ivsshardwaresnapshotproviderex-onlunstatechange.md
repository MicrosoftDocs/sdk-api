---
UID: NF:vsprov.IVssHardwareSnapshotProviderEx.OnLunStateChange
title: IVssHardwareSnapshotProviderEx::OnLunStateChange
author: windows-driver-content
description: The VSS service calls this method to notify hardware providers of a LUN state change.
old-location: base\ivsshardwaresnapshotproviderex_onlunstatechange.htm
old-project: VSS
ms.assetid: 7546eca0-db52-4c4b-9b5a-a3cfdf2a98af
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVssHardwareSnapshotProviderEx interface,OnLunStateChange method, IVssHardwareSnapshotProviderEx.OnLunStateChange, IVssHardwareSnapshotProviderEx::OnLunStateChange, OnLunStateChange, OnLunStateChange method, OnLunStateChange method,IVssHardwareSnapshotProviderEx interface, VSS_ONLUNSTATECHANGE_DO_MASK_LUNS, VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY, VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY, VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE, base.ivsshardwaresnapshotproviderex_onlunstatechange, vsprov/IVssHardwareSnapshotProviderEx::OnLunStateChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	IVssHardwareSnapshotProviderEx.OnLunStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssHardwareSnapshotProviderEx::OnLunStateChange


## -description


The VSS service calls this method to notify hardware providers of a LUN state change.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters




### -param pSnapshotLuns [in]

A pointer to an array of <i>dwCount</i> <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structures,  one for each LUN that contributes to the shadow copy volume.


### -param pOriginalLuns [in]

A pointer to an array of <i>dwCount</i> <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structures,  one for each LUN that contributes to the original volume.


### -param dwCount [in]

Number of elements in the <i>pSnapshotLuns</i> array. This is also the number of elements in the <i>pOriginalLuns</i> array.


### -param dwFlags [in]

A bitmask of <a href="https://msdn.microsoft.com/545977ae-7f62-4a8e-9d2f-936224f413b7">_VSS_HARDWARE_OPTIONS</a> flags that provide information about the state change that the shadow copy LUNs have undergone. The following table describes how each flag is used in this parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE"></a><a id="vss_onlunstatechange_notify_read_write"></a><dl>
<dt><b>VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The shadow copy LUN will be converted permanently to read-write.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY"></a><a id="vss_onlunstatechange_notify_lun_pre_recovery"></a><dl>
<dt><b>VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The shadow copy LUNs will be converted temporarily to read-write and are about to undergo TxF recovery or VSS auto-recovery.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY"></a><a id="vss_onlunstatechange_notify_lun_post_recovery"></a><dl>
<dt><b>VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The shadow copy LUNs have just undergone TxF recovery or VSS auto-recovery and have been converted back to read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="VSS_ONLUNSTATECHANGE_DO_MASK_LUNS"></a><a id="vss_onlunstatechange_do_mask_luns"></a><dl>
<dt><b>VSS_ONLUNSTATECHANGE_DO_MASK_LUNS</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The shadow copy LUNs must be masked from the current machine but not deleted.

</td>
</tr>
</table>
 


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
An unexpected provider error occurred. If this is returned, the error must be described in an entry in 
        the application event log, giving the user information on how to resolve the problem.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/aaf94823-845b-49cb-8599-962229fef4cb">IVssHardwareSnapshotProviderEx</a>
 

 

