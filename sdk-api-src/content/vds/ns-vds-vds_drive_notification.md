---
UID: NS:vds._VDS_DRIVE_NOTIFICATION
title: VDS_DRIVE_NOTIFICATION (vds.h)
description: The VDS_DRIVE_NOTIFICATION structure (vds.h) defines the details of drive events.
helpviewer_keywords: ["VDS_DRIVE_NOTIFICATION","VDS_DRIVE_NOTIFICATION structure [VDS]","VDS_NF_DRIVE_ARRIVE","VDS_NF_DRIVE_DEPART","VDS_NF_DRIVE_MODIFY","VDS_NF_DRIVE_REMOVED","base.vds_drive_notification","vds/_VDS_DRIVE_NOTIFICATION","vdshwprv/_VDS_DRIVE_NOTIFICATION"]
old-location: base\vds_drive_notification.htm
tech.root: base
ms.assetid: 933376b3-d5eb-407b-941c-4e2b61774c1a
ms.date: 08/05/2022
ms.keywords: VDS_DRIVE_NOTIFICATION, VDS_DRIVE_NOTIFICATION structure [VDS], VDS_NF_DRIVE_ARRIVE, VDS_NF_DRIVE_DEPART, VDS_NF_DRIVE_MODIFY, VDS_NF_DRIVE_REMOVED, base.vds_drive_notification, vds/_VDS_DRIVE_NOTIFICATION, vdshwprv/_VDS_DRIVE_NOTIFICATION
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
targetos: Windows
req.typenames: VDS_DRIVE_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DRIVE_NOTIFICATION
 - vds/_VDS_DRIVE_NOTIFICATION
 - VDS_DRIVE_NOTIFICATION
 - vds/VDS_DRIVE_NOTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_DRIVE_NOTIFICATION
---

# VDS_DRIVE_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of drive events.

## -struct-fields

### -field ulEvent

Determines the drive event for which an application will be notified, as one of the following values.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DRIVE_ARRIVE"></a><a id="vds_nf_drive_arrive"></a><dl>
<dt><b>VDS_NF_DRIVE_ARRIVE</b></dt>
<dt>105</dt>
</dl>
</td>
<td width="60%">
A drive is reported as physically present on the subsystem. The <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_status">VDS_DRIVE_STATUS</a> value associated with this notification should be any  value except <b>VDS_DRS_REMOVED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DRIVE_DEPART"></a><a id="vds_nf_drive_depart"></a><dl>
<dt><b>VDS_NF_DRIVE_DEPART</b></dt>
<dt>106</dt>
</dl>
</td>
<td width="60%">
A drive was physically removed from the subsystem. The <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_status">VDS_DRIVE_STATUS</a> value should be <b>VDS_DRS_UNKNOWN</b> or <b>VDS_DRS_REMOVED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DRIVE_MODIFY"></a><a id="vds_nf_drive_modify"></a><dl>
<dt><b>VDS_NF_DRIVE_MODIFY</b></dt>
<dt>107</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a> structure changed, or an extent on a drive changed.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DRIVE_REMOVED"></a><a id="vds_nf_drive_removed"></a><dl>
<dt><b>VDS_NF_DRIVE_REMOVED</b></dt>
<dt>354</dt>
</dl>
</td>
<td width="60%">
A drive that was in use as part of a RAID group or storage pool is no longer in use as part of the RAID group or storage pool. For example, if a RAID group drive was detected as failing and was replaced with a hot spare, the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_status">VDS_DRIVE_STATUS</a> value should be <b>VDS_DRS_FAILED</b>  (removed from use because of failure), <b>VDS_DRS_OFFLINE</b>  (not failed, but not in use), <b>VDS_DRS_NOT_READY</b>,  or <b>VDS_DRS_UNKNOWN</b>.
If the  drive was removed as part of rebalancing the storage, the drive is not failing, and the <b>VDS_DRIVE_STATUS</b> value should be <b>VDS_DRS_OFFLINE</b>  or <b>VDS_DRS_NOT_READY</b>.


<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

</td>
</tr>
</table>

### -field driveId

The GUID of the drive that triggered the event.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this structure as a member.

An application can receive drive events by implementing the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method.

To get the drive object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-getproperties">IVdsDrive::GetProperties</a> method or the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive2-getproperties2">IVdsDrive2::GetProperties2</a> method to get the drive properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
