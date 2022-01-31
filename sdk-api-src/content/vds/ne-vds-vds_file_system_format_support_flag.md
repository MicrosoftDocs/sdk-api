---
UID: NE:vds._VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
title: VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG (vds.h)
description: Defines the properties of file systems that are supported for formatting volumes.
helpviewer_keywords: ["VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG","VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG enumeration","VDS_FSS_DEFAULT","VDS_FSS_PREVIOUS_REVISION","VDS_FSS_RECOMMENDED","base.vds_file_system_format_support_flag","vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG","vds/VDS_FSS_DEFAULT","vds/VDS_FSS_PREVIOUS_REVISION","vds/VDS_FSS_RECOMMENDED"]
old-location: base\vds_file_system_format_support_flag.htm
tech.root: base
ms.assetid: 78d60240-44dc-48b8-b2a6-5babbd79085f
ms.date: 12/05/2018
ms.keywords: VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG, VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG enumeration, VDS_FSS_DEFAULT, VDS_FSS_PREVIOUS_REVISION, VDS_FSS_RECOMMENDED, base.vds_file_system_format_support_flag, vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG, vds/VDS_FSS_DEFAULT, vds/VDS_FSS_PREVIOUS_REVISION, vds/VDS_FSS_RECOMMENDED
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
 - vds/_VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
 - VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
 - vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
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
 - VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG
---

# VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of file systems that are supported for formatting volumes. These values are used in the <b>ulFlags</b> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_format_support_prop">VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP</a> structure.

## -enum-fields

### -field VDS_FSS_DEFAULT:0x1

The file system is the default file system to be used for formatting the volume.

### -field VDS_FSS_PREVIOUS_REVISION:0x2

The revision of the file system is not the latest revision supported for formatting the volume.

### -field VDS_FSS_RECOMMENDED:0x4

The file system is the recommended file system to be used for formatting the volume.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf2-formatpartitionex2">IVdsDiskPartitionMF2::FormatPartitionEx2</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-formatex">IVdsVolumeMF2::FormatEx</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_file_system_format_support_prop">VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP</a>
