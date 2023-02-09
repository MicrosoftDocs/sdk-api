---
UID: NS:vds._VDS_MOUNT_POINT_NOTIFICATION
title: VDS_MOUNT_POINT_NOTIFICATION (vds.h)
description: The VDS_MOUNT_POINT_NOTIFICATION structure (vds.h) represents notification information that was returned by the software provider because a drive letter or volume GUID path changed.
helpviewer_keywords: ["VDS_MOUNT_POINT_NOTIFICATION","VDS_MOUNT_POINT_NOTIFICATION structure [VDS]","VDS_NF_MOUNT_POINTS_CHANGE","base.vds_mount_point_notification","vds/_VDS_MOUNT_POINT_NOTIFICATION","vdshwprv/_VDS_MOUNT_POINT_NOTIFICATION"]
old-location: base\vds_mount_point_notification.htm
tech.root: base
ms.assetid: 6e49437e-8fc7-4fc5-a227-b326a1ea9967
ms.date: 08/05/2022
ms.keywords: VDS_MOUNT_POINT_NOTIFICATION, VDS_MOUNT_POINT_NOTIFICATION structure [VDS], VDS_NF_MOUNT_POINTS_CHANGE, base.vds_mount_point_notification, vds/_VDS_MOUNT_POINT_NOTIFICATION, vdshwprv/_VDS_MOUNT_POINT_NOTIFICATION
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
req.typenames: VDS_MOUNT_POINT_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_MOUNT_POINT_NOTIFICATION
 - vds/_VDS_MOUNT_POINT_NOTIFICATION
 - VDS_MOUNT_POINT_NOTIFICATION
 - vds/VDS_MOUNT_POINT_NOTIFICATION
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
 - VDS_MOUNT_POINT_NOTIFICATION
---

# VDS_MOUNT_POINT_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Represents notification information that was returned by the basic or dynamic software provider because a drive letter  or volume GUID path changed.

## -struct-fields

### -field ulEvent

Determines the event for which an application will be notified, as the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_MOUNT_POINTS_CHANGE"></a><a id="vds_nf_mount_points_change"></a><dl>
<dt><b>VDS_NF_MOUNT_POINTS_CHANGE</b></dt>
<dt>205</dt>
</dl>
</td>
<td width="60%">
The drive letter  or volume GUID path changed.

</td>
</tr>
</table>

### -field volumeId

The GUID of the volume object associated with the drive letter or volume GUID path that triggered the event.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive these event notifications by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
