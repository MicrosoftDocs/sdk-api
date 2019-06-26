---
UID: NE:imapi2._IMAPI_FORMAT2_DATA_MEDIA_STATE
title: IMAPI_FORMAT2_DATA_MEDIA_STATE (imapi2.h)
author: windows-sdk-content
description: Defines values for the possible media states.
old-location: imapi\imapi_format2_data_media_state.htm
tech.root: imapi
ms.assetid: 985001b9-e930-41fb-9a4c-94631c4aca70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PIMAPI_FORMAT2_DATA_MEDIA_STATE, IMAPI_FORMAT2_DATA_MEDIA_STATE, IMAPI_FORMAT2_DATA_MEDIA_STATE enumeration [IMAPI], IMAPI_FORMAT2_DATA_MEDIA_STATE_APPENDABLE, IMAPI_FORMAT2_DATA_MEDIA_STATE_BLANK, IMAPI_FORMAT2_DATA_MEDIA_STATE_DAMAGED, IMAPI_FORMAT2_DATA_MEDIA_STATE_ERASE_REQUIRED, IMAPI_FORMAT2_DATA_MEDIA_STATE_FINALIZED, IMAPI_FORMAT2_DATA_MEDIA_STATE_FINAL_SESSION, IMAPI_FORMAT2_DATA_MEDIA_STATE_INFORMATIONAL_MASK, IMAPI_FORMAT2_DATA_MEDIA_STATE_NON_EMPTY_SESSION, IMAPI_FORMAT2_DATA_MEDIA_STATE_OVERWRITE_ONLY, IMAPI_FORMAT2_DATA_MEDIA_STATE_RANDOMLY_WRITABLE, IMAPI_FORMAT2_DATA_MEDIA_STATE_UNKNOWN, IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MASK, IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MEDIA, IMAPI_FORMAT2_DATA_MEDIA_STATE_WRITE_PROTECTED, PIMAPI_FORMAT2_DATA_MEDIA_STATE, PIMAPI_FORMAT2_DATA_MEDIA_STATE enumeration pointer [IMAPI], imapi.imapi_format2_data_media_state, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_APPENDABLE, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_BLANK, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_DAMAGED, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_ERASE_REQUIRED, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_FINALIZED, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_FINAL_SESSION, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_INFORMATIONAL_MASK, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_NON_EMPTY_SESSION, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_OVERWRITE_ONLY, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_RANDOMLY_WRITABLE, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_UNKNOWN, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MASK, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MEDIA, imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE_WRITE_PROTECTED, imapi2/PIMAPI_FORMAT2_DATA_MEDIA_STATE"
ms.topic: enum
f1_keywords: 
 - "imapi2/IMAPI_FORMAT2_DATA_MEDIA_STATE"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - imapi2.h
api_name:
 - IMAPI_FORMAT2_DATA_MEDIA_STATE
product: Windows
targetos: Windows
req.typenames: IMAPI_FORMAT2_DATA_MEDIA_STATE, *PIMAPI_FORMAT2_DATA_MEDIA_STATE
req.redist: 
ms.custom: 19H1
---

# IMAPI_FORMAT2_DATA_MEDIA_STATE enumeration


## -description


Defines values for the possible media states.


## -enum-fields




### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_UNKNOWN

Indicates that the interface does not know the media state.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_INFORMATIONAL_MASK

Reports information (but not errors) about the media state.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MASK

Reports an unsupported media state.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_OVERWRITE_ONLY

Write operations can occur on used portions of the disc.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_RANDOMLY_WRITABLE

Media is randomly writable.  This indicates that a single session can be written to this disc.

<div class="alert"><b>Note</b>  This value is deprecated and superseded by <b>IMAPI_FORMAT2_DATA_MEDIA_STATE_OVERWRITE_ONLY</b>.</div>
<div> </div>

### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_BLANK

Media has never been used, or has been erased.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_APPENDABLE

Media is appendable (supports multiple sessions).


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_FINAL_SESSION

Media can have only one additional session added to it, or the media does not support multiple sessions.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_DAMAGED

Media is not usable by this interface.  The media might require an erase or other recovery.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_ERASE_REQUIRED

Media must be erased prior to use by this interface.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_NON_EMPTY_SESSION

Media has a partially written last session, which is not supported by this interface.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_WRITE_PROTECTED

Media or drive is write-protected.


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_FINALIZED

Media cannot be written to (finalized).


### -field IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MEDIA

Media is not supported by this interface.


## -remarks



This enumeration should be treated as a bitmask. Nearly all of the values set one bit set to one and the other bits to  zero.  Three exceptions to this rule were added: unknown, unsupported media mask, and informational mask.  For example, to test for unsupported media, check the value against IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MASK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_currentmediastatus">IDiscFormat2Data::get_CurrentMediaStatus</a>
 

 

