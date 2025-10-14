---
UID: NF:vsprov.IVssHardwareSnapshotProviderEx.OnLunStateChange
title: IVssHardwareSnapshotProviderEx::OnLunStateChange (vsprov.h)
description: The VSS service calls this method to notify hardware providers of a LUN state change.
helpviewer_keywords: ["IVssHardwareSnapshotProviderEx interface","OnLunStateChange method","IVssHardwareSnapshotProviderEx.OnLunStateChange","IVssHardwareSnapshotProviderEx::OnLunStateChange","OnLunStateChange","OnLunStateChange method","OnLunStateChange method","IVssHardwareSnapshotProviderEx interface","VSS_ONLUNSTATECHANGE_DO_MASK_LUNS","VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY","VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY","VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE","base.ivsshardwaresnapshotproviderex_onlunstatechange","vsprov/IVssHardwareSnapshotProviderEx::OnLunStateChange"]
old-location: base\ivsshardwaresnapshotproviderex_onlunstatechange.htm
tech.root: base
ms.assetid: 7546eca0-db52-4c4b-9b5a-a3cfdf2a98af
ms.date: 12/05/2018
ms.keywords: IVssHardwareSnapshotProviderEx interface,OnLunStateChange method, IVssHardwareSnapshotProviderEx.OnLunStateChange, IVssHardwareSnapshotProviderEx::OnLunStateChange, OnLunStateChange, OnLunStateChange method, OnLunStateChange method,IVssHardwareSnapshotProviderEx interface, VSS_ONLUNSTATECHANGE_DO_MASK_LUNS, VSS_ONLUNSTATECHANGE_NOTIFY_LUN_POST_RECOVERY, VSS_ONLUNSTATECHANGE_NOTIFY_LUN_PRE_RECOVERY, VSS_ONLUNSTATECHANGE_NOTIFY_READ_WRITE, base.ivsshardwaresnapshotproviderex_onlunstatechange, vsprov/IVssHardwareSnapshotProviderEx::OnLunStateChange
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssHardwareSnapshotProviderEx::OnLunStateChange
 - vsprov/IVssHardwareSnapshotProviderEx::OnLunStateChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssHardwareSnapshotProviderEx.OnLunStateChange
---

# IVssHardwareSnapshotProviderEx::OnLunStateChange


## -description

The VSS service calls this method to notify hardware providers of a LUN state change.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters

### -param pSnapshotLuns [in]

A pointer to an array of <i>dwCount</i> <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures,  one for each LUN that contributes to the shadow copy volume.

### -param pOriginalLuns [in]

A pointer to an array of <i>dwCount</i> <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures,  one for each LUN that contributes to the original volume.

### -param dwCount [in]

Number of elements in the <i>pSnapshotLuns</i> array. This is also the number of elements in the <i>pOriginalLuns</i> array.

### -param dwFlags [in]

A bitmask of <a href="/windows/desktop/api/vss/ne-vss-vss_hardware_options">_VSS_HARDWARE_OPTIONS</a> flags that provide information about the state change that the shadow copy LUNs have undergone. The following table describes how each flag is used in this parameter.

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
<dt><b>S_OK</b></dt>
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
<dt><b>E_OUTOFMEMORY</b></dt>
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
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
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

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotproviderex">IVssHardwareSnapshotProviderEx</a>