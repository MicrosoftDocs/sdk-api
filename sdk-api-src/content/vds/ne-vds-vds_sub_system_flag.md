---
UID: NE:vds._VDS_SUB_SYSTEM_FLAG
title: VDS_SUB_SYSTEM_FLAG
author: windows-sdk-content
description: Defines the set of valid flags for a subsystem object.
old-location: base\vds_sub_system_flag.htm
tech.root: vds
ms.assetid: 17a07d21-a10a-4f18-a975-def6db073256
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVDS_SUB_SYSTEM_FLAG, VDS_SF_CONSISTENCY_CHECK_CAPABLE, VDS_SF_DRIVE_EXTENT_CAPABLE, VDS_SF_HARDWARE_CHECKSUM_CAPABLE, VDS_SF_LUN_MASKING_CAPABLE, VDS_SF_LUN_PLEXING_CAPABLE, VDS_SF_LUN_REMAPPING_CAPABLE, VDS_SF_MEDIA_SCAN_CAPABLE, VDS_SF_RADIUS_CAPABLE, VDS_SF_READ_BACK_VERIFY_CAPABLE, VDS_SF_READ_CACHING_CAPABLE, VDS_SF_SUPPORTS_AUTH_CHAP, VDS_SF_SUPPORTS_AUTH_MUTUAL_CHAP, VDS_SF_SUPPORTS_FAULT_TOLERANT_LUNS, VDS_SF_SUPPORTS_LUN_NUMBER, VDS_SF_SUPPORTS_MIRRORED_CACHE, VDS_SF_SUPPORTS_MIRROR_LUNS, VDS_SF_SUPPORTS_NON_FAULT_TOLERANT_LUNS, VDS_SF_SUPPORTS_PARITY_LUNS, VDS_SF_SUPPORTS_SIMPLE_LUNS, VDS_SF_SUPPORTS_SIMPLE_TARGET_CONFIG, VDS_SF_SUPPORTS_SPAN_LUNS, VDS_SF_SUPPORTS_STRIPE_LUNS, VDS_SF_WRITE_CACHING_CAPABLE, VDS_SF_WRITE_THROUGH_CACHING_CAPABLE, VDS_SUB_SYSTEM_FLAG, VDS_SUB_SYSTEM_FLAG enumeration [VDS], base.vds_sub_system_flag, vds/VDS_SF_CONSISTENCY_CHECK_CAPABLE, vds/VDS_SF_DRIVE_EXTENT_CAPABLE, vds/VDS_SF_HARDWARE_CHECKSUM_CAPABLE, vds/VDS_SF_LUN_MASKING_CAPABLE, vds/VDS_SF_LUN_PLEXING_CAPABLE, vds/VDS_SF_LUN_REMAPPING_CAPABLE, vds/VDS_SF_MEDIA_SCAN_CAPABLE, vds/VDS_SF_RADIUS_CAPABLE, vds/VDS_SF_READ_BACK_VERIFY_CAPABLE, vds/VDS_SF_READ_CACHING_CAPABLE, vds/VDS_SF_SUPPORTS_AUTH_CHAP, vds/VDS_SF_SUPPORTS_AUTH_MUTUAL_CHAP, vds/VDS_SF_SUPPORTS_FAULT_TOLERANT_LUNS, vds/VDS_SF_SUPPORTS_LUN_NUMBER, vds/VDS_SF_SUPPORTS_MIRRORED_CACHE, vds/VDS_SF_SUPPORTS_MIRROR_LUNS, vds/VDS_SF_SUPPORTS_NON_FAULT_TOLERANT_LUNS, vds/VDS_SF_SUPPORTS_PARITY_LUNS, vds/VDS_SF_SUPPORTS_SIMPLE_LUNS, vds/VDS_SF_SUPPORTS_SIMPLE_TARGET_CONFIG, vds/VDS_SF_SUPPORTS_SPAN_LUNS, vds/VDS_SF_SUPPORTS_STRIPE_LUNS, vds/VDS_SF_WRITE_CACHING_CAPABLE, vds/VDS_SF_WRITE_THROUGH_CACHING_CAPABLE, vds/VDS_SUB_SYSTEM_FLAG, vdshwprv/VDS_SF_CONSISTENCY_CHECK_CAPABLE, vdshwprv/VDS_SF_DRIVE_EXTENT_CAPABLE, vdshwprv/VDS_SF_HARDWARE_CHECKSUM_CAPABLE, vdshwprv/VDS_SF_LUN_MASKING_CAPABLE, vdshwprv/VDS_SF_LUN_PLEXING_CAPABLE, vdshwprv/VDS_SF_LUN_REMAPPING_CAPABLE, vdshwprv/VDS_SF_MEDIA_SCAN_CAPABLE, vdshwprv/VDS_SF_RADIUS_CAPABLE, vdshwprv/VDS_SF_READ_BACK_VERIFY_CAPABLE, vdshwprv/VDS_SF_READ_CACHING_CAPABLE, vdshwprv/VDS_SF_SUPPORTS_AUTH_CHAP, vdshwprv/VDS_SF_SUPPORTS_AUTH_MUTUAL_CHAP, vdshwprv/VDS_SF_SUPPORTS_FAULT_TOLERANT_LUNS, vdshwprv/VDS_SF_SUPPORTS_LUN_NUMBER, vdshwprv/VDS_SF_SUPPORTS_MIRRORED_CACHE, vdshwprv/VDS_SF_SUPPORTS_MIRROR_LUNS, vdshwprv/VDS_SF_SUPPORTS_NON_FAULT_TOLERANT_LUNS, vdshwprv/VDS_SF_SUPPORTS_PARITY_LUNS, vdshwprv/VDS_SF_SUPPORTS_SIMPLE_LUNS, vdshwprv/VDS_SF_SUPPORTS_SIMPLE_TARGET_CONFIG, vdshwprv/VDS_SF_SUPPORTS_SPAN_LUNS, vdshwprv/VDS_SF_SUPPORTS_STRIPE_LUNS, vdshwprv/VDS_SF_WRITE_CACHING_CAPABLE, vdshwprv/VDS_SF_WRITE_THROUGH_CACHING_CAPABLE, vdshwprv/VDS_SUB_SYSTEM_FLAG"
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_SUB_SYSTEM_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_SUB_SYSTEM_FLAG, *PVDS_SUB_SYSTEM_FLAG
req.redist: 
---

# VDS_SUB_SYSTEM_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the set of valid flags for a subsystem object.


## -enum-fields




### -field VDS_SF_LUN_MASKING_CAPABLE

The subsystem supports LUN masking. This flag applies only to external hardware 
      providers—internal hardware providers do not support LUN masking.


### -field VDS_SF_LUN_PLEXING_CAPABLE

The provider supports LUNs with more than one plex.


### -field VDS_SF_LUN_REMAPPING_CAPABLE

The provider supports automatic remapping of LUN extents to drive extents.


### -field VDS_SF_DRIVE_EXTENT_CAPABLE

The provider supports the use of drive extents in LUN creation. If this flag is not set, the 
      provider uses only whole drives to create LUNs.


### -field VDS_SF_HARDWARE_CHECKSUM_CAPABLE

The provider supports verifying the integrity of the read and write data using a checksum. If this 
      flag is not set, the provider does not support using a checksum.


### -field VDS_SF_RADIUS_CAPABLE

The subsystem supports RADIUS.


### -field VDS_SF_READ_BACK_VERIFY_CAPABLE

The subsystem supports read verification of data that has been written.


### -field VDS_SF_WRITE_THROUGH_CACHING_CAPABLE

The subsystem supports write-through caching.


### -field VDS_SF_SUPPORTS_FAULT_TOLERANT_LUNS

The subsystem supports creation of automagic fault tolerant LUNs.


### -field VDS_SF_SUPPORTS_NON_FAULT_TOLERANT_LUNS

The subsystem supports creation of automagic non-fault tolerant LUNs.


### -field VDS_SF_SUPPORTS_SIMPLE_LUNS

The subsystem supports creation of simple LUNs.


### -field VDS_SF_SUPPORTS_SPAN_LUNS

The subsystem supports creation of spanned LUNs.


### -field VDS_SF_SUPPORTS_STRIPE_LUNS

The subsystem supports creation of striped LUNs.


### -field VDS_SF_SUPPORTS_MIRROR_LUNS

The subsystem supports creation of mirrored LUNs.


### -field VDS_SF_SUPPORTS_PARITY_LUNS

The subsystem supports creation of striped with parity LUNs.


### -field VDS_SF_SUPPORTS_AUTH_CHAP

The subsystem supports one-way CHAP authentication.


### -field VDS_SF_SUPPORTS_AUTH_MUTUAL_CHAP

The subsystem supports mutual CHAP authentication.


### -field VDS_SF_SUPPORTS_SIMPLE_TARGET_CONFIG

The subsystem supports only simple target configurations and automatically assigns LUNs to targets during LUN 
      creation. Such a target must be configured with at least one associated portal in the target's portal group. The provider is responsible for correctly associating portals with the target. A VDS application should not assume that the subsystem has the ability to create or delete simple targets.


### -field VDS_SF_SUPPORTS_LUN_NUMBER

The subsystem supports LUN numbering. See the <a href="https://msdn.microsoft.com/79aa7dc1-ef46-4b6d-8088-e42839625a16">IVdsLunNumber::GetLunNumber</a> method.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.


### -field VDS_SF_SUPPORTS_MIRRORED_CACHE

The subsystem supports LUNs that use a mirrored cache. See the <b>bUseMirroredCache</b> member of the <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.


### -field VDS_SF_READ_CACHING_CAPABLE

The subsystem supports read caching on LUNs. See the <b>VDS_LF_READ_CACHE_ENABLED</b> value of the <a href="https://msdn.microsoft.com/977ee10c-c91f-4510-bf00-6b7d4da6c1c0">VDS_LUN_FLAG</a> enumeration and the <b>bReadCachingEnabled</b> member of the <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.


### -field VDS_SF_WRITE_CACHING_CAPABLE

The subsystem supports write caching on LUNs. See the <b>VDS_LF_WRITE_CACHE_ENABLED</b> value of the <a href="https://msdn.microsoft.com/977ee10c-c91f-4510-bf00-6b7d4da6c1c0">VDS_LUN_FLAG</a> enumeration and the <b>bWriteCachingEnabled</b> member of the <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.


### -field VDS_SF_MEDIA_SCAN_CAPABLE

The subsystem supports media scanning on LUNs. See the <b>VDS_LF_MEDIA_SCAN_ENABLED</b> value of the <a href="https://msdn.microsoft.com/977ee10c-c91f-4510-bf00-6b7d4da6c1c0">VDS_LUN_FLAG</a> enumeration and the <b>bMediaScanEnabled</b> member of the <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.


### -field VDS_SF_CONSISTENCY_CHECK_CAPABLE

The subsystem supports consistency checking on LUNs. See the <b>VDS_LF_CONSISTENCY_CHECK_ENABLED</b> value of the <a href="https://msdn.microsoft.com/977ee10c-c91f-4510-bf00-6b7d4da6c1c0">VDS_LUN_FLAG</a> enumeration and the <b>bConsistencyCheckEnabled</b> member of the <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This flag is not supported.


## -remarks



This enumeration provides the values for the  <b>ulFlags</b> member of the 
    <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> and <a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a> structures.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_SUB_SYSTEM_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_SUB_SYSTEM_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a>



<a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a>
 

 

