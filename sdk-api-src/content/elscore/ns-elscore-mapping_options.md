---
UID: NS:elscore._MAPPING_OPTIONS
title: MAPPING_OPTIONS (elscore.h)
description: Contains options for text recognition. The values stored in this structure affect the behavior and results of MappingRecognizeText.
helpviewer_keywords: ["*PMAPPING_OPTIONS","MAPPING_OPTIONS","MAPPING_OPTIONS structure [Internationalization for Windows Applications]","PMAPPING_OPTIONS","PMAPPING_OPTIONS structure pointer [Internationalization for Windows Applications]","elscore/MAPPING_OPTIONS","elscore/PMAPPING_OPTIONS","intl.mappingoptions"]
old-location: intl\mappingoptions.htm
tech.root: Intl
ms.assetid: 228625b3-928c-451f-9a3f-7eb3130ac622
ms.date: 12/05/2018
ms.keywords: '*PMAPPING_OPTIONS, MAPPING_OPTIONS, MAPPING_OPTIONS structure [Internationalization for Windows Applications], PMAPPING_OPTIONS, PMAPPING_OPTIONS structure pointer [Internationalization for Windows Applications], elscore/MAPPING_OPTIONS, elscore/PMAPPING_OPTIONS, intl.mappingoptions'
req.header: elscore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: MAPPING_OPTIONS, *PMAPPING_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAPPING_OPTIONS
 - elscore/_MAPPING_OPTIONS
 - PMAPPING_OPTIONS
 - elscore/PMAPPING_OPTIONS
 - MAPPING_OPTIONS
 - elscore/MAPPING_OPTIONS
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
 - MAPPING_OPTIONS
---

# MAPPING_OPTIONS structure


## -description

Contains options for text recognition. The values stored in this structure affect the behavior and results of <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

## -struct-fields

### -field Size

Size of the structure, used to validate the structure version. This value is required.

### -field pszInputLanguage

Optional. Pointer to an input language string, following the IETF naming convention, that identifies the input language that the service should be able to accept. The application can set this member to <b>NULL</b> to indicate that the service is free to interpret the input as any input language it supports.

### -field pszOutputLanguage

Optional. Pointer to an output language string, following the IETF naming convention, that identifies the output language that the service should be able to use to produce results. The application can set this member to <b>NULL</b> if the service should decide the output language.

### -field pszInputScript

Optional. Pointer to a standard Unicode script name that should be accepted by the service. The application can set this member to <b>NULL</b> to let the service decide how handle the input.

### -field pszOutputScript

Optional. Pointer to a standard Unicode script name that the service should use to retrieve results. The application can set this member to <b>NULL</b> to let the service decide the output script.

### -field pszInputContentType

Optional. Pointer to a string, following the format of the MIME content types, that identifies the format that the service should be able to interpret when the application passes data. Examples of content types are "text/plain", "text/html", and "text/css". The application can set this member to <b>NULL</b> to indicate the "text/plain" content type. 

<div class="alert"><b>Note</b>  In Windows 7, the ELS services support only the content type "text/plain". A content type specification can be found at <a href="https://www.iana.org/assignments/media-types/text">Text Media Types</a>.</div>
<div> </div>

### -field pszOutputContentType

Optional. Pointer to a string, following the format of the MIME content types, that identifies the format in which the service should retrieve data. The application can set this member to <b>NULL</b> to let the service decide the output content type.

### -field pszUILanguage

Reserved.

### -field pfnRecognizeCallback

Optional. Pointer to an application callback function to receive callbacks with the results from the <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a> function. If a callback function is specified, text recognition is executed in asynchronous mode and the application obtains results through the callback function. The application must set this member to <b>NULL</b> if text recognition is to be synchronous.

### -field pRecognizeCallerData

Optional. Pointer to private application data passed to the callback function by a service after text recognition is complete. The application must set this member to <b>NULL</b> to indicate no private application data.

### -field dwRecognizeCallerDataSize

Optional. Size, in bytes, of any private application data indicated by the <b>pRecognizeCallerData</b> member.

### -field pfnActionCallback

Reserved.

### -field pActionCallerData

Reserved.

### -field dwActionCallerDataSize

Reserved.

### -field dwServiceFlag

Optional. Private flag that a service provider defines to affect service behavior. Services can interpret this flag as they require.

<div class="alert"><b>Note</b>  For Windows 7, none of the available ELS services support flags.</div>
<div> </div>

### -field GetActionDisplayName

Reserved.

## -remarks

The application does not have to fill in all members of this structure, as services treat <b>NULL</b> members as default values. All unused members must be set to 0.

<div class="alert"><b>Warning</b>  The data passed in this structure to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>, as well as data referred to by the <i>pszText</i> argument in that call, 

must remain valid until the property bag structure passed by <i>pBag</i> is freed via 

<a href="/windows/desktop/api/elscore/nf-elscore-mappingfreepropertybag">MappingFreePropertyBag</a>. This is because both synchronous and asynchronous calls to 

<b>MappingRecognizeText</b> and <a href="/windows/desktop/api/elscore/nf-elscore-mappingdoaction">MappingDoAction</a> will attempt to use the data passed to the initial 

call to <b>MappingRecognizeText</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services-structures">Extended Linguistic Services Structures</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_data_range">MAPPING_DATA_RANGE</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>