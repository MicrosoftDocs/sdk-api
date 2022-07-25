---
UID: NE:vds.tag_VDS_PARTITION_STYLE
title: __VDS_PARTITION_STYLE (vds.h)
description: This enumeration is not for explicit use.
helpviewer_keywords: ["VDS_PARTITION_STYLE_GPT","VDS_PARTITION_STYLE_MBR","VDS_PARTITION_STYLE_RAW","__VDS_PARTITION_STYLE","__VDS_PARTITION_STYLE enumeration [VDS]","base.tag_vds_partition_style","tag_VDS_PARTITION_STYLE","tag_VDS_PARTITION_STYLE enumeration [VDS]","vds/VDS_PARTITION_STYLE_GPT","vds/VDS_PARTITION_STYLE_MBR","vds/VDS_PARTITION_STYLE_RAW","vds/tag_VDS_PARTITION_STYLE"]
old-location: base\tag_vds_partition_style.htm
tech.root: base
ms.assetid: d994715e-1735-4841-98be-5f22de0670f0
ms.date: 12/05/2018
ms.keywords: VDS_PARTITION_STYLE_GPT, VDS_PARTITION_STYLE_MBR, VDS_PARTITION_STYLE_RAW, __VDS_PARTITION_STYLE, __VDS_PARTITION_STYLE enumeration [VDS], base.tag_vds_partition_style, tag_VDS_PARTITION_STYLE, tag_VDS_PARTITION_STYLE enumeration [VDS], vds/VDS_PARTITION_STYLE_GPT, vds/VDS_PARTITION_STYLE_MBR, vds/VDS_PARTITION_STYLE_RAW, vds/tag_VDS_PARTITION_STYLE
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
req.typenames: __VDS_PARTITION_STYLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_VDS_PARTITION_STYLE
 - vds/tag_VDS_PARTITION_STYLE
 - __VDS_PARTITION_STYLE
 - vds/__VDS_PARTITION_STYLE
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
 - __VDS_PARTITION_STYLE
---

# __VDS_PARTITION_STYLE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

This enumeration is 
   not for explicit use.

## -enum-fields

### -field VDS_PARTITION_STYLE_MBR:0

This value is not intended for use.

### -field VDS_PARTITION_STYLE_GPT

This value is not intended for use.

### -field VDS_PARTITION_STYLE_RAW

This value is not intended for use.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>tag_VDS_PARTITION_STYLE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>tag_VDS_PARTITION_STYLE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>
