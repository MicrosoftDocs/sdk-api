---
UID: NE:vds._VDS_PARTITION_FLAG
title: VDS_PARTITION_FLAG (vds.h)
description: Defines a set of valid flags for a partition.
helpviewer_keywords: ["VDS_PARTITION_FLAG","VDS_PARTITION_FLAG enumeration [VDS]","VDS_PTF_SYSTEM","base.vds_partition_flag","vds/VDS_PARTITION_FLAG","vds/VDS_PTF_SYSTEM"]
old-location: base\vds_partition_flag.htm
tech.root: base
ms.assetid: d6ac5769-d0bc-4a4e-93c0-e9c83303ec4c
ms.date: 12/05/2018
ms.keywords: VDS_PARTITION_FLAG, VDS_PARTITION_FLAG enumeration [VDS], VDS_PTF_SYSTEM, base.vds_partition_flag, vds/VDS_PARTITION_FLAG, vds/VDS_PTF_SYSTEM
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
req.typenames: VDS_PARTITION_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PARTITION_FLAG
 - vds/_VDS_PARTITION_FLAG
 - VDS_PARTITION_FLAG
 - vds/VDS_PARTITION_FLAG
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
 - VDS_PARTITION_FLAG
---

# VDS_PARTITION_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a set of valid flags for a partition.

## -enum-fields

### -field VDS_PTF_SYSTEM:0x1

If set, the partition is a system partition.

## -remarks

This enumeration provides the values for the <i>ulFlags</i> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_partition_prop">VDS_PARTITION_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PARTITION_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PARTITION_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_prop">VDS_PARTITION_PROP</a>
