---
UID: NC:elscore.PFN_MAPPINGCALLBACKPROC
title: PFN_MAPPINGCALLBACKPROC (elscore.h)
description: An application-defined callback function that asynchronously processes data produced by the MappingRecognizeText function.
helpviewer_keywords: ["MappingCallbackProc","MappingCallbackProc callback function [Internationalization for Windows Applications]","PFN_MAPPINGCALLBACKPROC","PFN_MAPPINGCALLBACKPROC callback","elscore/MappingCallbackProc","intl.mappingcallbackproc"]
old-location: intl\mappingcallbackproc.htm
tech.root: Intl
ms.assetid: 7a324708-4f1b-467c-af1a-da36d1f7eba0
ms.date: 12/05/2018
ms.keywords: MappingCallbackProc, MappingCallbackProc callback function [Internationalization for Windows Applications], PFN_MAPPINGCALLBACKPROC, PFN_MAPPINGCALLBACKPROC callback, elscore/MappingCallbackProc, intl.mappingcallbackproc
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_MAPPINGCALLBACKPROC
 - elscore/PFN_MAPPINGCALLBACKPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Elscore.h
api_name:
 - MappingCallbackProc
---

# PFN_MAPPINGCALLBACKPROC callback function


## -description

An application-defined callback function that asynchronously processes data produced by the <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a> function. The <b>MAPPINGCALLBACKPROC</b> type defines a pointer to this callback function. <b>MappingCallbackProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param pBag [in]

Pointer to a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a> structure containing the results of the call to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

### -param data [in]

Pointer to private application data. This pointer is the same as that passed in the <b>pRecognizeCallerData</b> member of the <a href="/windows/desktop/api/elscore/ns-elscore-mapping_options">MAPPING_OPTIONS</a> structure.

### -param dwDataSize [in]

Size, in bytes, of the private application data. This size is the same as that passed in the <b>dwRecognizeCallerDataSize</b> member of the <a href="/windows/desktop/api/elscore/ns-elscore-mapping_options">MAPPING_OPTIONS</a> structure when the application calls <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a> asynchronously.

### -param Result [in]

Return code from <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>. The return code is S_OK if the function succeeded, or an error code otherwise.

## -remarks

A <b>MappingCallbackProc</b> function consumes the results retrieved by <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>. The application registers the callback function by passing its address to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a> in a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_options">MAPPING_OPTIONS</a> structure.

The application should check the <i>Result</i> parameter before using the data in the <i>pBag</i> parameter. When it is done using the data from the property bag, the application must call <a href="/windows/desktop/api/elscore/nf-elscore-mappingfreepropertybag">MappingFreePropertyBag</a> because the property bag can contain pointers into the original text. For more information about the property bag, see the remarks for the <a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a> structure.

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services">Extended Linguistic Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services-functions">Extended Linguistic Services Functions</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_options">MAPPING_OPTIONS</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>



<a href="/windows/desktop/Intl/providing-callbacks-for-els-services">Providing Callbacks for ELS Services</a>
