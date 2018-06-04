---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _IMAPI_FORMAT2_DATA_MEDIA_STATE enumeration


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




<a href="https://msdn.microsoft.com/b8ed119f-8976-48aa-ab9a-86c1361b6e14">IDiscFormat2Data::get_CurrentMediaStatus</a>
 

 

