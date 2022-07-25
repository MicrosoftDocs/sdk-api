---
UID: NE:vds._VDS_FILE_SYSTEM_PROP_FLAG
title: VDS_FILE_SYSTEM_PROP_FLAG (vds.h)
description: Defines the details of file-system compression.
helpviewer_keywords: ["VDS_FILE_SYSTEM_PROP_FLAG","VDS_FILE_SYSTEM_PROP_FLAG enumeration [VDS]","VDS_FPF_COMPRESSED","base.vds_file_system_prop_flag","vds/VDS_FILE_SYSTEM_PROP_FLAG","vds/VDS_FPF_COMPRESSED"]
old-location: base\vds_file_system_prop_flag.htm
tech.root: base
ms.assetid: f2776ee9-4809-4f99-b464-80b5b53f8675
ms.date: 12/05/2018
ms.keywords: VDS_FILE_SYSTEM_PROP_FLAG, VDS_FILE_SYSTEM_PROP_FLAG enumeration [VDS], VDS_FPF_COMPRESSED, base.vds_file_system_prop_flag, vds/VDS_FILE_SYSTEM_PROP_FLAG, vds/VDS_FPF_COMPRESSED
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
req.typenames: VDS_FILE_SYSTEM_PROP_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FILE_SYSTEM_PROP_FLAG
 - vds/_VDS_FILE_SYSTEM_PROP_FLAG
 - VDS_FILE_SYSTEM_PROP_FLAG
 - vds/VDS_FILE_SYSTEM_PROP_FLAG
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
 - VDS_FILE_SYSTEM_PROP_FLAG
---

# VDS_FILE_SYSTEM_PROP_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of file-system compression.

## -enum-fields

### -field VDS_FPF_COMPRESSED:0x1

If set, the file system supports file compression.

## -remarks

This enumeration provides the values for the <i>ulFlags</i> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FILE_SYSTEM_PROP_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FILE_SYSTEM_PROP_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a>
