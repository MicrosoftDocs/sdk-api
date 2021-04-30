---
UID: NF:elscore.MappingRecognizeText
title: MappingRecognizeText function (elscore.h)
description: Calls upon an ELS service to recognize text. For example, the Microsoft Language Detection service will attempt to recognize the language in which the input text is written.
helpviewer_keywords: ["MappingRecognizeText","MappingRecognizeText function [Internationalization for Windows Applications]","elscore/MappingRecognizeText","intl.mappingrecognizetext"]
old-location: intl\mappingrecognizetext.htm
tech.root: Intl
ms.assetid: 49f30bdd-4612-423b-9913-9c35ad8a88d5
ms.date: 12/05/2018
ms.keywords: MappingRecognizeText, MappingRecognizeText function [Internationalization for Windows Applications], elscore/MappingRecognizeText, intl.mappingrecognizetext
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
 - MappingRecognizeText
 - elscore/MappingRecognizeText
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
 - MappingRecognizeText
---

# MappingRecognizeText function


## -description

Calls upon an ELS service to recognize text. For example, the Microsoft Language Detection service will attempt to recognize the language in which the input text is written.

## -parameters

### -param pServiceInfo [in]

Pointer to a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_service_info">MAPPING_SERVICE_INFO</a> structure containing information about the service to use in text recognition. The structure must be one of the structures retrieved by a previous call to <a href="/windows/desktop/api/elscore/nf-elscore-mappinggetservices">MappingGetServices</a>. This parameter cannot be set to <b>NULL</b>.

### -param pszText [in]

Pointer to the text to recognize. The text must be UTF-16, but some services have additional requirements for the input format. This parameter cannot be set to <b>NULL</b>.

### -param dwLength [in]

Length, in characters, of the text specified in <i>pszText</i>.

### -param dwIndex [in]

Index inside the specified text to be used by the service. This value should be between 0 and <i>dwLength</i>-1. If the application wants to process the entire text, it should set this parameter to 0.

### -param pOptions [in, optional]

Pointer to a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_options">MAPPING_OPTIONS</a> structure containing options that affect the result and behavior of text recognition. The application does not have to specify values for all structure members. This parameter can be set to <b>NULL</b> to use the default mapping options.

### -param pbag [in, out]

Pointer to a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a> structure in which the service stores its results. On input, the application passes a structure with only the size provided, and the other members set to 0. On output, the structure is filled with information produced by the service during text recognition. This parameter cannot be set to <b>NULL</b>.

## -returns

Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.

## -remarks

The type of text to recognize depends on the service type used by the application. For more information, see <a href="/windows/desktop/Intl/requesting-text-recognition">Requesting Text Recognition</a>.

<div class="alert"><b>Warning</b>  The data referred to by <i>pszText</i> and <i>pOptions</i> must remain valid until the property bag structure passed by <i>pBag</i> is freed via 

<a href="/windows/desktop/api/elscore/nf-elscore-mappingfreepropertybag">MappingFreePropertyBag</a>. This is because both synchronous and asynchronous calls to 

<b>MappingRecognizeText</b> and <a href="/windows/desktop/api/elscore/nf-elscore-mappingdoaction">MappingDoAction</a> will attempt to use the data passed to the initial 

call to <b>MappingRecognizeText</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services">Extended Linguistic Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services-functions">Extended Linguistic Services Functions</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_options">MAPPING_OPTIONS</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_service_info">MAPPING_SERVICE_INFO</a>



<a href="/windows/desktop/Intl/requesting-text-recognition">Requesting Text Recognition</a>