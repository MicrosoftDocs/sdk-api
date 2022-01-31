---
UID: NE:vds._VDS_LUN_FLAG
title: VDS_LUN_FLAG (vds.h)
description: Defines the set of valid flags for a LUN object.
helpviewer_keywords: ["*PVDS_LUN_FLAG","VDS_LF_CONSISTENCY_CHECK_ENABLED","VDS_LF_HARDWARE_CHECKSUM_ENABLED","VDS_LF_LBN_REMAP_ENABLED","VDS_LF_MEDIA_SCAN_ENABLED","VDS_LF_READ_BACK_VERIFY_ENABLED","VDS_LF_READ_CACHE_ENABLED","VDS_LF_SNAPSHOT","VDS_LF_WRITE_CACHE_ENABLED","VDS_LF_WRITE_THROUGH_CACHING_ENABLED","VDS_LUN_FLAG","VDS_LUN_FLAG enumeration [VDS]","base.vds_lun_flag","vds/VDS_LF_CONSISTENCY_CHECK_ENABLED","vds/VDS_LF_HARDWARE_CHECKSUM_ENABLED","vds/VDS_LF_LBN_REMAP_ENABLED","vds/VDS_LF_MEDIA_SCAN_ENABLED","vds/VDS_LF_READ_BACK_VERIFY_ENABLED","vds/VDS_LF_READ_CACHE_ENABLED","vds/VDS_LF_SNAPSHOT","vds/VDS_LF_WRITE_CACHE_ENABLED","vds/VDS_LF_WRITE_THROUGH_CACHING_ENABLED","vds/VDS_LUN_FLAG","vdshwprv/VDS_LF_CONSISTENCY_CHECK_ENABLED","vdshwprv/VDS_LF_HARDWARE_CHECKSUM_ENABLED","vdshwprv/VDS_LF_LBN_REMAP_ENABLED","vdshwprv/VDS_LF_MEDIA_SCAN_ENABLED","vdshwprv/VDS_LF_READ_BACK_VERIFY_ENABLED","vdshwprv/VDS_LF_READ_CACHE_ENABLED","vdshwprv/VDS_LF_SNAPSHOT","vdshwprv/VDS_LF_WRITE_CACHE_ENABLED","vdshwprv/VDS_LF_WRITE_THROUGH_CACHING_ENABLED","vdshwprv/VDS_LUN_FLAG"]
old-location: base\vds_lun_flag.htm
tech.root: base
ms.assetid: 977ee10c-c91f-4510-bf00-6b7d4da6c1c0
ms.date: 12/05/2018
ms.keywords: '*PVDS_LUN_FLAG, VDS_LF_CONSISTENCY_CHECK_ENABLED, VDS_LF_HARDWARE_CHECKSUM_ENABLED, VDS_LF_LBN_REMAP_ENABLED, VDS_LF_MEDIA_SCAN_ENABLED, VDS_LF_READ_BACK_VERIFY_ENABLED, VDS_LF_READ_CACHE_ENABLED, VDS_LF_SNAPSHOT, VDS_LF_WRITE_CACHE_ENABLED, VDS_LF_WRITE_THROUGH_CACHING_ENABLED, VDS_LUN_FLAG, VDS_LUN_FLAG enumeration [VDS], base.vds_lun_flag, vds/VDS_LF_CONSISTENCY_CHECK_ENABLED, vds/VDS_LF_HARDWARE_CHECKSUM_ENABLED, vds/VDS_LF_LBN_REMAP_ENABLED, vds/VDS_LF_MEDIA_SCAN_ENABLED, vds/VDS_LF_READ_BACK_VERIFY_ENABLED, vds/VDS_LF_READ_CACHE_ENABLED, vds/VDS_LF_SNAPSHOT, vds/VDS_LF_WRITE_CACHE_ENABLED, vds/VDS_LF_WRITE_THROUGH_CACHING_ENABLED, vds/VDS_LUN_FLAG, vdshwprv/VDS_LF_CONSISTENCY_CHECK_ENABLED, vdshwprv/VDS_LF_HARDWARE_CHECKSUM_ENABLED, vdshwprv/VDS_LF_LBN_REMAP_ENABLED, vdshwprv/VDS_LF_MEDIA_SCAN_ENABLED, vdshwprv/VDS_LF_READ_BACK_VERIFY_ENABLED, vdshwprv/VDS_LF_READ_CACHE_ENABLED, vdshwprv/VDS_LF_SNAPSHOT, vdshwprv/VDS_LF_WRITE_CACHE_ENABLED, vdshwprv/VDS_LF_WRITE_THROUGH_CACHING_ENABLED, vdshwprv/VDS_LUN_FLAG'
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
req.typenames: VDS_LUN_FLAG, *PVDS_LUN_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_FLAG
 - vds/_VDS_LUN_FLAG
 - PVDS_LUN_FLAG
 - vds/PVDS_LUN_FLAG
 - VDS_LUN_FLAG
 - vds/VDS_LUN_FLAG
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
 - VDS_LUN_FLAG
---

# VDS_LUN_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for a LUN object.

## -enum-fields

### -field VDS_LF_LBN_REMAP_ENABLED:0x1

The provider remaps LUN extents to drive extents automatically.

### -field VDS_LF_READ_BACK_VERIFY_ENABLED:0x2

The provider verifies writes by readback.

### -field VDS_LF_WRITE_THROUGH_CACHING_ENABLED:0x4

The provider enables write-through caching on the LUN.

### -field VDS_LF_HARDWARE_CHECKSUM_ENABLED:0x8

The provider verifies the integrity of the read and write data using a checksum.

### -field VDS_LF_READ_CACHE_ENABLED:0x10

Read caching is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

### -field VDS_LF_WRITE_CACHE_ENABLED:0x20

Write caching is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

### -field VDS_LF_MEDIA_SCAN_ENABLED:0x40

Media scanning is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

### -field VDS_LF_CONSISTENCY_CHECK_ENABLED:0x80

Consistency checking is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

### -field VDS_LF_SNAPSHOT:0x100

The LUN is a volume shadow copy LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.

## -remarks

This enumeration provides the values for the <i>ulFlags</i> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_prop">VDS_LUN_PROP</a> structure and provides the value for the <b>VDS_LPF_LBN_REMAP_ENABLED</b> enumerator in the <a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_flag">VDS_LUN_PLEX_FLAG</a> enumeration.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_lun_plex_flag">VDS_LUN_PLEX_FLAG</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_prop">VDS_LUN_PROP</a>
