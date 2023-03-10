---
UID: NE:imapi2._IMAPI_CD_SECTOR_TYPE
title: IMAPI_CD_SECTOR_TYPE (imapi2.h)
description: Defines the sector types that can be written to CD media.
helpviewer_keywords: ["*PIMAPI_CD_SECTOR_TYPE","IMAPI_CD_SECTOR_AUDIO","IMAPI_CD_SECTOR_MODE1","IMAPI_CD_SECTOR_MODE1RAW","IMAPI_CD_SECTOR_MODE2FORM0","IMAPI_CD_SECTOR_MODE2FORM0RAW","IMAPI_CD_SECTOR_MODE2FORM1","IMAPI_CD_SECTOR_MODE2FORM1RAW","IMAPI_CD_SECTOR_MODE2FORM2","IMAPI_CD_SECTOR_MODE2FORM2RAW","IMAPI_CD_SECTOR_MODE_ZERO","IMAPI_CD_SECTOR_TYPE","IMAPI_CD_SECTOR_TYPE enumeration [IMAPI]","imapi.imapi_cd_sector_type","imapi2/IMAPI_CD_SECTOR_AUDIO","imapi2/IMAPI_CD_SECTOR_MODE1","imapi2/IMAPI_CD_SECTOR_MODE1RAW","imapi2/IMAPI_CD_SECTOR_MODE2FORM0","imapi2/IMAPI_CD_SECTOR_MODE2FORM0RAW","imapi2/IMAPI_CD_SECTOR_MODE2FORM1","imapi2/IMAPI_CD_SECTOR_MODE2FORM1RAW","imapi2/IMAPI_CD_SECTOR_MODE2FORM2","imapi2/IMAPI_CD_SECTOR_MODE2FORM2RAW","imapi2/IMAPI_CD_SECTOR_MODE_ZERO","imapi2/IMAPI_CD_SECTOR_TYPE"]
old-location: imapi\imapi_cd_sector_type.htm
tech.root: imapi
ms.assetid: 3af4a8c9-66b7-490e-aafa-fdfe614f5f3e
ms.date: 12/05/2018
ms.keywords: '*PIMAPI_CD_SECTOR_TYPE, IMAPI_CD_SECTOR_AUDIO, IMAPI_CD_SECTOR_MODE1, IMAPI_CD_SECTOR_MODE1RAW, IMAPI_CD_SECTOR_MODE2FORM0, IMAPI_CD_SECTOR_MODE2FORM0RAW, IMAPI_CD_SECTOR_MODE2FORM1, IMAPI_CD_SECTOR_MODE2FORM1RAW, IMAPI_CD_SECTOR_MODE2FORM2, IMAPI_CD_SECTOR_MODE2FORM2RAW, IMAPI_CD_SECTOR_MODE_ZERO, IMAPI_CD_SECTOR_TYPE, IMAPI_CD_SECTOR_TYPE enumeration [IMAPI], imapi.imapi_cd_sector_type, imapi2/IMAPI_CD_SECTOR_AUDIO, imapi2/IMAPI_CD_SECTOR_MODE1, imapi2/IMAPI_CD_SECTOR_MODE1RAW, imapi2/IMAPI_CD_SECTOR_MODE2FORM0, imapi2/IMAPI_CD_SECTOR_MODE2FORM0RAW, imapi2/IMAPI_CD_SECTOR_MODE2FORM1, imapi2/IMAPI_CD_SECTOR_MODE2FORM1RAW, imapi2/IMAPI_CD_SECTOR_MODE2FORM2, imapi2/IMAPI_CD_SECTOR_MODE2FORM2RAW, imapi2/IMAPI_CD_SECTOR_MODE_ZERO, imapi2/IMAPI_CD_SECTOR_TYPE'
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
req.typenames: IMAPI_CD_SECTOR_TYPE, *PIMAPI_CD_SECTOR_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAPI_CD_SECTOR_TYPE
 - imapi2/_IMAPI_CD_SECTOR_TYPE
 - PIMAPI_CD_SECTOR_TYPE
 - imapi2/PIMAPI_CD_SECTOR_TYPE
 - IMAPI_CD_SECTOR_TYPE
 - imapi2/IMAPI_CD_SECTOR_TYPE
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
 - IMAPI_CD_SECTOR_TYPE
---

# IMAPI_CD_SECTOR_TYPE enumeration


## -description

Defines the sector types that can be written to CD media.

## -enum-fields

### -field IMAPI_CD_SECTOR_AUDIO:0

With this sector type, Audio data has 2352 bytes per sector/frame.  This can be broken down into 588 contiguous samples, each sample being four bytes.  The layout of a single sample matches the 16-bit stereo 44.1KHz WAV file data.  This type of sector has no additional error correcting codes.

### -field IMAPI_CD_SECTOR_MODE_ZERO:0x1

With this sector type, user data has 2336 bytes per sector/frame.  This seldom-used sector type contains all zero data, and is almost never seen in media today.

### -field IMAPI_CD_SECTOR_MODE1:0x2

With this sector type, user data has 2048 bytes per sector/frame.  Mode1 data is the most common data form for pressed CD-ROM media.  This data type also provides the greatest level of ECC/EDC among the standard sector types.

### -field IMAPI_CD_SECTOR_MODE2FORM0:0x3

With this sector type, user data has 2336 bytes per sector/frame.  All Mode 2 sector types are also known as "CD-ROM XA" modes, which allows mixing of audio and data tracks on a single disc.  This sector type is also known as Mode 2 "Formless", is considered deprecated, and is very seldom used.

### -field IMAPI_CD_SECTOR_MODE2FORM1:0x4

With this sector type, user data has 2048 bytes per sector/frame.  All Mode 2 sector types are also known as "CD-ROM XA" modes, which allows mixing of audio and data tracks on a single disc.

### -field IMAPI_CD_SECTOR_MODE2FORM2:0x5

With this sector type, user data has 2336 bytes per sector/frame, of which the final four bytes are an optional CRC code (zero if not used).  All Mode 2 sector types are also known as "CD-ROM XA" modes, which allows mixing of audio and data tracks on a single disc.  This sector type is most often used when writing VideoCD discs.

### -field IMAPI_CD_SECTOR_MODE1RAW:0x6

With this sector type, user data has 2352 bytes per sector/frame.  This is pre-processed Mode1Cooked data sectors, with sector header, ECC/EDC, and scrambling already added to the data stream.

### -field IMAPI_CD_SECTOR_MODE2FORM0RAW:0x7

With this sector type, user data has 2352 bytes per sector/frame.  This is pre-processed Mode2Form0 data sectors, with sector header, ECC/EDC, and scrambling already added to the data stream.

### -field IMAPI_CD_SECTOR_MODE2FORM1RAW:0x8

With this sector type, user data has 2352 bytes per sector/frame.  This is pre-processed Mode2Form1 data sectors, with sector header, ECC/EDC, and scrambling already added to the data stream.

### -field IMAPI_CD_SECTOR_MODE2FORM2RAW:0x9

With this sector type, user data has 2352 bytes per sector/frame.  This is pre-processed Mode2Form2 data sectors, with sector header, ECC/EDC, and scrambling already added to the data stream.

## -remarks

Some sector types are not compatible with other sector types within a single image.  The following are typical examples of this condition:

<ul>
<li>If the first track is audio, then all tracks must be audio.</li>
<li>If the first track is Mode1, then all tracks must be Mode1.</li>
<li>Only the three Mode2 (XA) sectors (Mode 2 Form 0, Mode 2 Form 1, and Mode 2 Form 2) may be mixed within a single disc image, and even then, only with other Mode 2 (XA) sector types.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>
