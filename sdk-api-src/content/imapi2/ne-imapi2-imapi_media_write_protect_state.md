---
UID: NE:imapi2._IMAPI_MEDIA_WRITE_PROTECT_STATE
title: IMAPI_MEDIA_WRITE_PROTECT_STATE (imapi2.h)
description: Defines values that indicate the media write protect status. One or more write protect values can be set on a given drive.
helpviewer_keywords: ["*PIMAPI_MEDIA_WRITE_PROTECT_STATE","IMAPI_MEDIA_WRITE_PROTECT_STATE","IMAPI_MEDIA_WRITE_PROTECT_STATE enumeration [IMAPI]","IMAPI_WRITEPROTECTED_BY_CARTRIDGE","IMAPI_WRITEPROTECTED_BY_DISC_CONTROL_BLOCK","IMAPI_WRITEPROTECTED_BY_MEDIA_SPECIFIC_REASON","IMAPI_WRITEPROTECTED_BY_SOFTWARE_WRITE_PROTECT","IMAPI_WRITEPROTECTED_READ_ONLY_MEDIA","IMAPI_WRITEPROTECTED_UNTIL_POWERDOWN","PIMAPI_MEDIA_WRITE_PROTECT_STATE","PIMAPI_MEDIA_WRITE_PROTECT_STATE enumeration pointer [IMAPI]","imapi.imapi_media_write_protect_state","imapi2/IMAPI_MEDIA_WRITE_PROTECT_STATE","imapi2/IMAPI_WRITEPROTECTED_BY_CARTRIDGE","imapi2/IMAPI_WRITEPROTECTED_BY_DISC_CONTROL_BLOCK","imapi2/IMAPI_WRITEPROTECTED_BY_MEDIA_SPECIFIC_REASON","imapi2/IMAPI_WRITEPROTECTED_BY_SOFTWARE_WRITE_PROTECT","imapi2/IMAPI_WRITEPROTECTED_READ_ONLY_MEDIA","imapi2/IMAPI_WRITEPROTECTED_UNTIL_POWERDOWN","imapi2/PIMAPI_MEDIA_WRITE_PROTECT_STATE"]
old-location: imapi\imapi_media_write_protect_state.htm
tech.root: imapi
ms.assetid: fe58b469-0294-49b6-bfcf-7632de36833e
ms.date: 12/05/2018
ms.keywords: '*PIMAPI_MEDIA_WRITE_PROTECT_STATE, IMAPI_MEDIA_WRITE_PROTECT_STATE, IMAPI_MEDIA_WRITE_PROTECT_STATE enumeration [IMAPI], IMAPI_WRITEPROTECTED_BY_CARTRIDGE, IMAPI_WRITEPROTECTED_BY_DISC_CONTROL_BLOCK, IMAPI_WRITEPROTECTED_BY_MEDIA_SPECIFIC_REASON, IMAPI_WRITEPROTECTED_BY_SOFTWARE_WRITE_PROTECT, IMAPI_WRITEPROTECTED_READ_ONLY_MEDIA, IMAPI_WRITEPROTECTED_UNTIL_POWERDOWN, PIMAPI_MEDIA_WRITE_PROTECT_STATE, PIMAPI_MEDIA_WRITE_PROTECT_STATE enumeration pointer [IMAPI], imapi.imapi_media_write_protect_state, imapi2/IMAPI_MEDIA_WRITE_PROTECT_STATE, imapi2/IMAPI_WRITEPROTECTED_BY_CARTRIDGE, imapi2/IMAPI_WRITEPROTECTED_BY_DISC_CONTROL_BLOCK, imapi2/IMAPI_WRITEPROTECTED_BY_MEDIA_SPECIFIC_REASON, imapi2/IMAPI_WRITEPROTECTED_BY_SOFTWARE_WRITE_PROTECT, imapi2/IMAPI_WRITEPROTECTED_READ_ONLY_MEDIA, imapi2/IMAPI_WRITEPROTECTED_UNTIL_POWERDOWN, imapi2/PIMAPI_MEDIA_WRITE_PROTECT_STATE'
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IMAPI_MEDIA_WRITE_PROTECT_STATE, *PIMAPI_MEDIA_WRITE_PROTECT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAPI_MEDIA_WRITE_PROTECT_STATE
 - imapi2/_IMAPI_MEDIA_WRITE_PROTECT_STATE
 - PIMAPI_MEDIA_WRITE_PROTECT_STATE
 - imapi2/PIMAPI_MEDIA_WRITE_PROTECT_STATE
 - IMAPI_MEDIA_WRITE_PROTECT_STATE
 - imapi2/IMAPI_MEDIA_WRITE_PROTECT_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - imapi2.h
api_name:
 - IMAPI_MEDIA_WRITE_PROTECT_STATE
---

# IMAPI_MEDIA_WRITE_PROTECT_STATE enumeration


## -description

Defines values that indicate the media write protect status.   One or more write protect values can be set on a given drive.

## -enum-fields

### -field IMAPI_WRITEPROTECTED_UNTIL_POWERDOWN:0x1

  Power to the drive needs to be cycled before allowing writes to the media.

### -field IMAPI_WRITEPROTECTED_BY_CARTRIDGE:0x2

The media is in a cartridge with the write protect tab set.

### -field IMAPI_WRITEPROTECTED_BY_MEDIA_SPECIFIC_REASON:0x4

The drive is disallowing writes for a media-specific reason. For example:  <ul>
<li>The media was originally in a cartridge and was set to disallow writes when the media is not in a cartridge.</li>
<li>The media has used all available spare areas for defect management and is preventing writes to protect the existing data.</li>
</ul>

### -field IMAPI_WRITEPROTECTED_BY_SOFTWARE_WRITE_PROTECT:0x8

A write-protect flag on the media is set. Various media types, such as DVD-RAM and DVD-RW, support a special area on the media to indicate the disc's write protect status.

### -field IMAPI_WRITEPROTECTED_BY_DISC_CONTROL_BLOCK:0x10

A write-protect flag in the disc control block of a DVD+RW disc is set. DVD+RW media can persistently alter the write protect state of media by writing a device control block (DCB) to the media.  

This value has limited usefulness because some DVD+RW drives do not recognize or honor this setting.

### -field IMAPI_WRITEPROTECTED_READ_ONLY_MEDIA:0x4000

The drive does not recognize write capability of the media.

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_writeprotectstatus">IDiscFormat2Data::get_WriteProtectStatus</a>
