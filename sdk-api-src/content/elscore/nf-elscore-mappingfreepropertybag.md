---
UID: NF:elscore.MappingFreePropertyBag
title: MappingFreePropertyBag function (elscore.h)
description: Frees memory and resources allocated during an ELS text recognition operation.
helpviewer_keywords: ["MappingFreePropertyBag","MappingFreePropertyBag function [Internationalization for Windows Applications]","elscore/MappingFreePropertyBag","intl.mappingfreepropertybag"]
old-location: intl\mappingfreepropertybag.htm
tech.root: Intl
ms.assetid: 7e06e85d-109a-4c5f-be18-3750e25c4986
ms.date: 12/05/2018
ms.keywords: MappingFreePropertyBag, MappingFreePropertyBag function [Internationalization for Windows Applications], elscore/MappingFreePropertyBag, intl.mappingfreepropertybag
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
req.lib: Elscore.lib
req.dll: Elscore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MappingFreePropertyBag
 - elscore/MappingFreePropertyBag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Elscore.dll
 - ext-ms-win-els-elscore-l1-1-0.dll
api_name:
 - MappingFreePropertyBag
---

# MappingFreePropertyBag function


## -description

Frees memory and resources allocated during an ELS text recognition operation.

## -parameters

### -param pBag [in]

Pointer to a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a> structure containing the properties for which to free resources. This parameter cannot be set to <b>NULL</b>.

## -returns

Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.

## -remarks

An ELS service allocates memory and resources for data retrieved from application calls to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>. The <b>MappingFreePropertyBag</b> function releases these resources.

<div class="alert"><b>Caution</b>  Services should not be freed before freeing the property bags produced by those services.</div>
<div> </div>
<div class="alert"><b>Caution</b>  The application must call this function only once for each call to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a> when the property bag is no longer needed. Not calling <b>MappingFreePropertyBag</b> after each call to <b>MappingRecognizeText</b> causes a resource leak. For more information about memory allocation for the property bag, see the remarks for the <a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a> structure.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services">Extended Linguistic Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services-functions">Extended Linguistic Services Functions</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>



<a href="/windows/desktop/Intl/requesting-text-recognition">Requesting Text Recognition</a>