---
UID: NE:vds._VDS_DISK_OFFLINE_REASON
title: VDS_DISK_OFFLINE_REASON (vds.h)
description: Defines the set of reasons for a disk to be offline.
helpviewer_keywords: ["VDSDiskOfflineReasonCollision","VDSDiskOfflineReasonNone","VDSDiskOfflineReasonPolicy","VDSDiskOfflineReasonRedundantPath","VDSDiskOfflineReasonSnapshot","VDS_DISK_OFFLINE_REASON","VDS_DISK_OFFLINE_REASON enumeration","base.vds_disk_offline_reason","vds/VDSDiskOfflineReasonCollision","vds/VDSDiskOfflineReasonNone","vds/VDSDiskOfflineReasonPolicy","vds/VDSDiskOfflineReasonRedundantPath","vds/VDSDiskOfflineReasonSnapshot","vds/VDS_DISK_OFFLINE_REASON"]
old-location: base\vds_disk_offline_reason.htm
tech.root: base
ms.assetid: 45115cd5-52bb-4cb8-978b-208a2bc3c148
ms.date: 12/05/2018
ms.keywords: VDSDiskOfflineReasonCollision, VDSDiskOfflineReasonNone, VDSDiskOfflineReasonPolicy, VDSDiskOfflineReasonRedundantPath, VDSDiskOfflineReasonSnapshot, VDS_DISK_OFFLINE_REASON, VDS_DISK_OFFLINE_REASON enumeration, base.vds_disk_offline_reason, vds/VDSDiskOfflineReasonCollision, vds/VDSDiskOfflineReasonNone, vds/VDSDiskOfflineReasonPolicy, vds/VDSDiskOfflineReasonRedundantPath, vds/VDSDiskOfflineReasonSnapshot, vds/VDS_DISK_OFFLINE_REASON
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_DISK_OFFLINE_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DISK_OFFLINE_REASON
 - vds/_VDS_DISK_OFFLINE_REASON
 - VDS_DISK_OFFLINE_REASON
 - vds/VDS_DISK_OFFLINE_REASON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_DISK_OFFLINE_REASON
---

# VDS_DISK_OFFLINE_REASON enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of reasons for a disk to be offline.

## -enum-fields

### -field VDSDiskOfflineReasonNone:0

The reason is unknown.

### -field VDSDiskOfflineReasonPolicy:1

The disk is offline because of the current <a href="/windows/desktop/api/vds/ne-vds-vds_san_policy">SAN policy</a>.

### -field VDSDiskOfflineReasonRedundantPath:2

The disk is offline because it has a path that is the same as that of another device. This value is used when multipathing is physically enabled, but the MPIO software is not installed or is not functioning properly. (When the MPIO software is functioning properly, it exposes only one disk device.)

### -field VDSDiskOfflineReasonSnapshot:3

The disk is offline because it contains a volume shadow copy volume. In this case, the disk is a clone of another disk that is online.

### -field VDSDiskOfflineReasonCollision:4

If the disk is an MBR disk, it is offline because its disk signature is the same as that of another disk that is online. The disk signature is found in the <b>dwSignature</b> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> and <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a> structures and in the <b>Signature</b> member of the <a href="/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_mbr">DRIVE_LAYOUT_INFORMATION_MBR</a> structure.

If it is a GPT disk, it is offline for one of the following reasons:<ul>
<li>Its disk identifier is the same as that of another disk that is offline. The disk identifier is found in the <b>DiskGuid</b> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> and <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a> structures and in the <b>DiskId</b> member of the <a href="/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_gpt">DRIVE_LAYOUT_INFORMATION_GPT</a> structure.</li>
<li>One of the partitions has the same partition GUID as another partition on the same disk.</li>
</ul>

### -field VDSDiskOfflineReasonResourceExhaustion:5

### -field VDSDiskOfflineReasonWriteFailure:6

### -field VDSDiskOfflineReasonDIScan:7

### -field VDSDiskOfflineReasonLostDataPersistence:8

## -see-also

<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>
