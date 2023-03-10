---
UID: NS:vds._VDS_DRIVE_LETTER_PROP
title: VDS_DRIVE_LETTER_PROP (vds.h)
description: Defines the properties of a drive letter.
helpviewer_keywords: ["*PVDS_DRIVE_LETTER_PROP","PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE","PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE structure pointer [VDS]","VDS_DRIVE_LETTER_PROP","VDS_DRIVE_LETTER_PROP structure [VDS]","base.vds_drive_letter_prop","vds/PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE","vds/_VDS_DRIVE_LETTER_PROP"]
old-location: base\vds_drive_letter_prop.htm
tech.root: base
ms.assetid: b944e29a-85b0-4cab-b804-1a09a19caddb
ms.date: 12/05/2018
ms.keywords: '*PVDS_DRIVE_LETTER_PROP, PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE, PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE structure pointer [VDS], VDS_DRIVE_LETTER_PROP, VDS_DRIVE_LETTER_PROP structure [VDS], base.vds_drive_letter_prop, vds/PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE, vds/_VDS_DRIVE_LETTER_PROP'
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
req.typenames: VDS_DRIVE_LETTER_PROP, *PVDS_DRIVE_LETTER_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DRIVE_LETTER_PROP
 - vds/_VDS_DRIVE_LETTER_PROP
 - PVDS_DRIVE_LETTER_PROP
 - vds/PVDS_DRIVE_LETTER_PROP
 - VDS_DRIVE_LETTER_PROP
 - vds/VDS_DRIVE_LETTER_PROP
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
 - VDS_DRIVE_LETTER_PROP
---

# VDS_DRIVE_LETTER_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a drive letter.

## -struct-fields

### -field wcLetter

The drive letter.

### -field volumeId

The GUID of the volume object represented by the drive letter.

### -field ulFlags

The drive letter flags enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_drive_letter_flag">VDS_DRIVE_LETTER_FLAG</a>.

### -field bUsed

If true, the drive letter is already in use; otherwise, the drive letter is available.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-querydriveletters">IVdsService::QueryDriveLetters</a> method returns this structure to report the property details of a drive letter.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-querydriveletters">IVdsService::QueryDriveLetters</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_drive_letter_flag">VDS_DRIVE_LETTER_FLAG</a>