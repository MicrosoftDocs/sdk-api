---
UID: NE:imapi2._IMAPI_FORMAT2_RAW_CD_WRITE_ACTION
title: IMAPI_FORMAT2_RAW_CD_WRITE_ACTION (imapi2.h)
description: Defines values that indicate the current state of the write operation when using the IDiscFormat2RawCDEventArgs interface.
helpviewer_keywords: ["*PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION","IMAPI_FORMAT2_RAW_CD_WRITE_ACTION","IMAPI_FORMAT2_RAW_CD_WRITE_ACTION enumeration [IMAPI]","IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_FINISHING","IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_PREPARING","IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_UNKNOWN","IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_WRITING","PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION","PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION enumeration pointer [IMAPI]","imapi.imapi_format2_raw_cd_write_action","imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION","imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_FINISHING","imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_PREPARING","imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_UNKNOWN","imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_WRITING","imapi2/PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION"]
old-location: imapi\imapi_format2_raw_cd_write_action.htm
tech.root: imapi
ms.assetid: eb19b3e1-59b2-4649-87c5-057d50213ef2
ms.date: 12/05/2018
ms.keywords: '*PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION, IMAPI_FORMAT2_RAW_CD_WRITE_ACTION, IMAPI_FORMAT2_RAW_CD_WRITE_ACTION enumeration [IMAPI], IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_FINISHING, IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_PREPARING, IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_UNKNOWN, IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_WRITING, PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION, PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION enumeration pointer [IMAPI], imapi.imapi_format2_raw_cd_write_action, imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION, imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_FINISHING, imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_PREPARING, imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_UNKNOWN, imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_WRITING, imapi2/PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION'
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
req.typenames: IMAPI_FORMAT2_RAW_CD_WRITE_ACTION, *PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAPI_FORMAT2_RAW_CD_WRITE_ACTION
 - imapi2/_IMAPI_FORMAT2_RAW_CD_WRITE_ACTION
 - PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION
 - imapi2/PIMAPI_FORMAT2_RAW_CD_WRITE_ACTION
 - IMAPI_FORMAT2_RAW_CD_WRITE_ACTION
 - imapi2/IMAPI_FORMAT2_RAW_CD_WRITE_ACTION
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
 - IMAPI_FORMAT2_RAW_CD_WRITE_ACTION
---

# IMAPI_FORMAT2_RAW_CD_WRITE_ACTION enumeration


## -description

Defines values that indicate the current state of the write operation when using the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs">IDiscFormat2RawCDEventArgs</a> interface.

## -enum-fields

### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_UNKNOWN:0

Indicates an unknown state.

### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_PREPARING:0x1

Preparing to write the session.

### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_WRITING:0x2

Writing session data.

### -field IMAPI_FORMAT2_RAW_CD_WRITE_ACTION_FINISHING:0x3

Synchronizing the drive's cache with the end of the data written to disc.

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2rawcdevents-update">DDiscFormat2RawCDEvents::Update</a>
