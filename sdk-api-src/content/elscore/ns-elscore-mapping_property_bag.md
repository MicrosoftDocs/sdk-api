---
UID: NS:elscore._MAPPING_PROPERTY_BAG
title: MAPPING_PROPERTY_BAG (elscore.h)
description: Contains the text recognition data properties retrieved by MappingRecognizeText.
helpviewer_keywords: ["*PMAPPING_PROPERTY_BAG","MAPPING_PROPERTY_BAG","MAPPING_PROPERTY_BAG structure [Internationalization for Windows Applications]","PMAPPING_PROPERTY_BAG","PMAPPING_PROPERTY_BAG structure pointer [Internationalization for Windows Applications]","elscore/MAPPING_PROPERTY_BAG","elscore/PMAPPING_PROPERTY_BAG","intl.mappingpropertybag"]
old-location: intl\mappingpropertybag.htm
tech.root: Intl
ms.assetid: 08e55e27-5118-40ea-b973-cea0b1c263da
ms.date: 12/05/2018
ms.keywords: '*PMAPPING_PROPERTY_BAG, MAPPING_PROPERTY_BAG, MAPPING_PROPERTY_BAG structure [Internationalization for Windows Applications], PMAPPING_PROPERTY_BAG, PMAPPING_PROPERTY_BAG structure pointer [Internationalization for Windows Applications], elscore/MAPPING_PROPERTY_BAG, elscore/PMAPPING_PROPERTY_BAG, intl.mappingpropertybag'
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
req.typenames: MAPPING_PROPERTY_BAG, *PMAPPING_PROPERTY_BAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAPPING_PROPERTY_BAG
 - elscore/_MAPPING_PROPERTY_BAG
 - PMAPPING_PROPERTY_BAG
 - elscore/PMAPPING_PROPERTY_BAG
 - MAPPING_PROPERTY_BAG
 - elscore/MAPPING_PROPERTY_BAG
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
 - MAPPING_PROPERTY_BAG
---

# MAPPING_PROPERTY_BAG structure


## -description

Contains the text recognition data properties retrieved by <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

## -struct-fields

### -field Size

Size of the structure, used to verify the structure version. This value is required.

### -field prgResultRanges

Pointer to an array of <a href="/windows/desktop/api/elscore/ns-elscore-mapping_data_range">MAPPING_DATA_RANGE</a> structures containing all recognized text range results. This member is populated by <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

### -field dwRangesCount

Number of items in the array indicated by <b>prgResultRanges</b>. This member is populated by <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

### -field pServiceData

Pointer to private service data. The service can document the format of this data so that the application can use it. The service also manages the memory for this data. This member is populated by <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

### -field dwServiceDataSize

Size, in bytes, of the private service data specified by <b>pServiceData</b>. The size is set to 0 if there is no private data. This member is populated by <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

### -field pCallerData

Pointer to private application data to pass to the service. The application manages the memory for this data.

### -field dwCallerDataSize

Size, in bytes, of the private application data indicated in <b>pCallerData</b>. This member is set to 0 if there is no private data.

### -field pContext

Reserved for internal use.

## -remarks

The memory for the property bag structure itself is managed by the application. The ELS platform and its services only manage the data pointers that they store in the property bag.

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services-structures">Extended Linguistic Services Structures</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_data_range">MAPPING_DATA_RANGE</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>