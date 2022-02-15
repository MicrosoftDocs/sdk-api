---
UID: NE:vds._VDS_FORMAT_OPTION_FLAGS
title: VDS_FORMAT_OPTION_FLAGS (vds.h)
description: Defines the set of valid formatting options for the IVdsDiskPartitionMF2::FormatPartitionEx2 method.
helpviewer_keywords: ["VDS_FORMAT_OPTION_FLAGS","VDS_FORMAT_OPTION_FLAGS enumeration","VDS_FSOF_COMPRESSION","VDS_FSOF_DUPLICATE_METADATA","VDS_FSOF_FORCE","VDS_FSOF_NONE","VDS_FSOF_QUICK","base.vds_format_option_flags","vds/VDS_FORMAT_OPTION_FLAGS","vds/VDS_FSOF_COMPRESSION","vds/VDS_FSOF_DUPLICATE_METADATA","vds/VDS_FSOF_FORCE","vds/VDS_FSOF_NONE","vds/VDS_FSOF_QUICK"]
old-location: base\vds_format_option_flags.htm
tech.root: base
ms.assetid: 75c92a9a-36c9-4c8d-90f2-a2b88cd8a7b5
ms.date: 12/05/2018
ms.keywords: VDS_FORMAT_OPTION_FLAGS, VDS_FORMAT_OPTION_FLAGS enumeration, VDS_FSOF_COMPRESSION, VDS_FSOF_DUPLICATE_METADATA, VDS_FSOF_FORCE, VDS_FSOF_NONE, VDS_FSOF_QUICK, base.vds_format_option_flags, vds/VDS_FORMAT_OPTION_FLAGS, vds/VDS_FSOF_COMPRESSION, vds/VDS_FSOF_DUPLICATE_METADATA, vds/VDS_FSOF_FORCE, vds/VDS_FSOF_NONE, vds/VDS_FSOF_QUICK
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
req.typenames: VDS_FORMAT_OPTION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FORMAT_OPTION_FLAGS
 - vds/_VDS_FORMAT_OPTION_FLAGS
 - VDS_FORMAT_OPTION_FLAGS
 - vds/VDS_FORMAT_OPTION_FLAGS
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
 - VDS_FORMAT_OPTION_FLAGS
---

# VDS_FORMAT_OPTION_FLAGS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid formatting options for the <a href="/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf2-formatpartitionex2">IVdsDiskPartitionMF2::FormatPartitionEx2</a> method.

## -enum-fields

### -field VDS_FSOF_NONE:0

No options are specified.

### -field VDS_FSOF_FORCE:0x1

The format operation should be forced, even if the partition is in use.

### -field VDS_FSOF_QUICK:0x2

Perform a quick format operation. A quick format does not verify each sector on the volume.

### -field VDS_FSOF_COMPRESSION:0x4

Enable compression on the newly formatted file system volume. Compression is a feature of the NTFS file system; it cannot be set for other file systems such as FAT or FAT32.

### -field VDS_FSOF_DUPLICATE_METADATA:0x8

Forces duplication of metadata for UDF 2.5 and above.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FORMAT_OPTION_FLAGS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FORMAT_OPTION_FLAGS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf2-formatpartitionex2">IVdsDiskPartitionMF2::FormatPartitionEx2</a>
