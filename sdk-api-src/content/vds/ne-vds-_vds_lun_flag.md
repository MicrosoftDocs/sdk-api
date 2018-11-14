---
UID: NE:vds._VDS_LUN_FLAG
title: "_VDS_LUN_FLAG"
author: windows-sdk-content
description: Defines the set of valid flags for a LUN object.
old-location: base\vds_lun_flag.htm
tech.root: VDS
ms.assetid: 977ee10c-c91f-4510-bf00-6b7d4da6c1c0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PVDS_LUN_FLAG, VDS_LF_CONSISTENCY_CHECK_ENABLED, VDS_LF_HARDWARE_CHECKSUM_ENABLED, VDS_LF_LBN_REMAP_ENABLED, VDS_LF_MEDIA_SCAN_ENABLED, VDS_LF_READ_BACK_VERIFY_ENABLED, VDS_LF_READ_CACHE_ENABLED, VDS_LF_SNAPSHOT, VDS_LF_WRITE_CACHE_ENABLED, VDS_LF_WRITE_THROUGH_CACHING_ENABLED, VDS_LUN_FLAG, VDS_LUN_FLAG enumeration [VDS], _VDS_LUN_FLAG, base.vds_lun_flag, vds/VDS_LF_CONSISTENCY_CHECK_ENABLED, vds/VDS_LF_HARDWARE_CHECKSUM_ENABLED, vds/VDS_LF_LBN_REMAP_ENABLED, vds/VDS_LF_MEDIA_SCAN_ENABLED, vds/VDS_LF_READ_BACK_VERIFY_ENABLED, vds/VDS_LF_READ_CACHE_ENABLED, vds/VDS_LF_SNAPSHOT, vds/VDS_LF_WRITE_CACHE_ENABLED, vds/VDS_LF_WRITE_THROUGH_CACHING_ENABLED, vds/VDS_LUN_FLAG, vdshwprv/VDS_LF_CONSISTENCY_CHECK_ENABLED, vdshwprv/VDS_LF_HARDWARE_CHECKSUM_ENABLED, vdshwprv/VDS_LF_LBN_REMAP_ENABLED, vdshwprv/VDS_LF_MEDIA_SCAN_ENABLED, vdshwprv/VDS_LF_READ_BACK_VERIFY_ENABLED, vdshwprv/VDS_LF_READ_CACHE_ENABLED, vdshwprv/VDS_LF_SNAPSHOT, vdshwprv/VDS_LF_WRITE_CACHE_ENABLED, vdshwprv/VDS_LF_WRITE_THROUGH_CACHING_ENABLED, vdshwprv/VDS_LUN_FLAG"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - VDS_LUN_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_LUN_FLAG, *PVDS_LUN_FLAG
req.redist: 
---

# _VDS_LUN_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for a LUN object.


## -enum-fields




### -field VDS_LF_LBN_REMAP_ENABLED

The provider remaps LUN extents to drive extents automatically.


### -field VDS_LF_READ_BACK_VERIFY_ENABLED

The provider verifies writes by readback.


### -field VDS_LF_WRITE_THROUGH_CACHING_ENABLED

The provider enables write-through caching on the LUN.


### -field VDS_LF_HARDWARE_CHECKSUM_ENABLED

The provider verifies the integrity of the read and write data using a checksum.


### -field VDS_LF_READ_CACHE_ENABLED

Read caching is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_WRITE_CACHE_ENABLED

Write caching is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_MEDIA_SCAN_ENABLED

Media scanning is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_CONSISTENCY_CHECK_ENABLED

Consistency checking is enabled on the LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LF_SNAPSHOT

The LUN is a volume shadow copy LUN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



This enumeration provides the values for the <i>ulFlags</i> member of the <a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a> structure and provides the value for the <b>VDS_LPF_LBN_REMAP_ENABLED</b> enumerator in the <a href="https://msdn.microsoft.com/0258d87c-0270-449e-8e96-2c511c5f7242">VDS_LUN_PLEX_FLAG</a> enumeration.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/0258d87c-0270-449e-8e96-2c511c5f7242">VDS_LUN_PLEX_FLAG</a>



<a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a>
 

 

