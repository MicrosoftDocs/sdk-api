---
UID: NE:vds._VDS_DRIVE_LETTER_FLAG
title: VDS_DRIVE_LETTER_FLAG (vds.h)
description: Defines the set of valid flags for a drive letter.
helpviewer_keywords: ["VDS_DLF_NON_PERSISTENT","VDS_DRIVE_LETTER_FLAG","VDS_DRIVE_LETTER_FLAG enumeration [VDS]","base.vds_drive_letter_flag","vds/VDS_DLF_NON_PERSISTENT","vds/VDS_DRIVE_LETTER_FLAG"]
old-location: base\vds_drive_letter_flag.htm
tech.root: base
ms.assetid: f6eebe08-ebc9-45d3-a752-9cdc13f9bcf1
ms.date: 12/05/2018
ms.keywords: VDS_DLF_NON_PERSISTENT, VDS_DRIVE_LETTER_FLAG, VDS_DRIVE_LETTER_FLAG enumeration [VDS], base.vds_drive_letter_flag, vds/VDS_DLF_NON_PERSISTENT, vds/VDS_DRIVE_LETTER_FLAG
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
req.typenames: VDS_DRIVE_LETTER_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DRIVE_LETTER_FLAG
 - vds/_VDS_DRIVE_LETTER_FLAG
 - VDS_DRIVE_LETTER_FLAG
 - vds/VDS_DRIVE_LETTER_FLAG
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
 - VDS_DRIVE_LETTER_FLAG
---

# VDS_DRIVE_LETTER_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for a drive letter.

## -enum-fields

### -field VDS_DLF_NON_PERSISTENT:0x1

If set, the drive letter disappears after the computer reboots.

## -remarks

This enumeration provides the values for the <i>ulFlags</i> member of the <a href="/windows/desktop/api/vds/ns-vds-vds_drive_letter_prop">VDS_DRIVE_LETTER_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_DRIVE_LETTER_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_DRIVE_LETTER_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
