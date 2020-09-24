---
UID: NS:elscore._MAPPING_DATA_RANGE
title: MAPPING_DATA_RANGE (elscore.h)
description: Contains text recognition results for a recognized text subrange. An array of structures of this type is retrieved by an Extended Linguistic Services (ELS) service in a MAPPING_PROPERTY_BAG structure.
helpviewer_keywords: ["*PMAPPING_DATA_RANGE","MAPPING_DATA_RANGE","MAPPING_DATA_RANGE structure [Internationalization for Windows Applications]","PMAPPING_DATA_RANGE","PMAPPING_DATA_RANGE structure pointer [Internationalization for Windows Applications]","elscore/MAPPING_DATA_RANGE","elscore/PMAPPING_DATA_RANGE","intl.mappingdatarange"]
old-location: intl\mappingdatarange.htm
tech.root: Intl
ms.assetid: adff7901-1903-45dd-888f-1b8c5bb05de1
ms.date: 12/05/2018
ms.keywords: '*PMAPPING_DATA_RANGE, MAPPING_DATA_RANGE, MAPPING_DATA_RANGE structure [Internationalization for Windows Applications], PMAPPING_DATA_RANGE, PMAPPING_DATA_RANGE structure pointer [Internationalization for Windows Applications], elscore/MAPPING_DATA_RANGE, elscore/PMAPPING_DATA_RANGE, intl.mappingdatarange'
req.header: elscore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MAPPING_DATA_RANGE, *PMAPPING_DATA_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAPPING_DATA_RANGE
 - elscore/_MAPPING_DATA_RANGE
 - PMAPPING_DATA_RANGE
 - elscore/PMAPPING_DATA_RANGE
 - MAPPING_DATA_RANGE
 - elscore/MAPPING_DATA_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Elscore.h
api_name:
 - MAPPING_DATA_RANGE
---

# MAPPING_DATA_RANGE structure


## -description

Contains text recognition results for a recognized text subrange. An array of structures of this type is retrieved by an Extended Linguistic Services (ELS) service in a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a> structure.

## -struct-fields

### -field dwStartIndex

Index of the beginning of the subrange in the text, where 0 indicates the character at the pointer passed to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>, instead of an offset to the index passed to the function in the <i>dwIndex</i> parameter. The value should be less than the entire length of the text.

### -field dwEndIndex

Index of the end of the subrange in the text, where 0 indicates the character at the pointer passed to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>, instead of an offset to the index passed to the function in the <i>dwIndex</i> parameter. The value should be less than the entire length of the text.

### -field pszDescription

Reserved.

### -field dwDescriptionLength

Reserved.

### -field pData

Pointer to data retrieved as service output associated with the subrange. This data must be of the format indicated by the content type supplied in the <b>pszContentType</b> member.

### -field dwDataSize

Size, in bytes, of the data specified in <b>pData</b>. Each service is required to report its output data size in bytes.

### -field pszContentType

Optional. Pointer to a string specifying the MIME content type of the data indicated by <b>pData</b>. Examples of content types are "text/plain", "text/html", and "text/css". 

<div class="alert"><b>Note</b>  In Windows 7, the ELS services support only the content type "text/plain". A content type specification can be found at <a href="https://www.iana.org/assignments/media-types/text">Text Media Types</a>.</div>
<div> </div>

### -field prgActionIds

Available action Ids for this subrange. They are usable for calling <a href="/windows/desktop/api/elscore/nf-elscore-mappingdoaction">MappingDoAction</a>.

<div class="alert"><b>Note</b>  In Windows 7, the ELS services do not expose any actions.</div>
<div> </div>

### -field dwActionsCount

The number of available actions for this subrange.

<div class="alert"><b>Note</b>  In Windows 7, the ELS services do not expose any actions.</div>
<div> </div>

### -field prgActionDisplayNames

Action display names for this subrange. These strings can be localized.

<div class="alert"><b>Note</b>  In Windows 7, the ELS services do not expose any actions.</div>
<div> </div>

## -remarks

<div class="alert"><b>Note</b>  The application should not alter any of the members of this data structure.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services-structures">Extended Linguistic Services Structures</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a>