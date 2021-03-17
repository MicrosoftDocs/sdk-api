---
UID: NF:elscore.MappingDoAction
title: MappingDoAction function (elscore.h)
description: Causes an ELS service to perform an action after text recognition has occurred. For example, a phone dialer service first must recognize phone numbers and then can perform the &quot;action&quot; of dialing a number.
helpviewer_keywords: ["MappingDoAction","MappingDoAction function [Internationalization for Windows Applications]","elscore/MappingDoAction","intl.mappingdoaction"]
old-location: intl\mappingdoaction.htm
tech.root: Intl
ms.assetid: c3903d10-3429-4707-82b5-33efa6b2dc4c
ms.date: 12/05/2018
ms.keywords: MappingDoAction, MappingDoAction function [Internationalization for Windows Applications], elscore/MappingDoAction, intl.mappingdoaction
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
req.lib: Elscore.lib
req.dll: Elscore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MappingDoAction
 - elscore/MappingDoAction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Elscore.dll
api_name:
 - MappingDoAction
---

# MappingDoAction function


## -description

Causes an ELS service to perform an action after text recognition has occurred. For example, a phone dialer service first must recognize phone numbers and then can perform the "action" of dialing a number.

## -parameters

### -param pBag [in, out]

Pointer to a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a> structure containing the results of a previous call to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>. This parameter cannot be set to <b>NULL</b>.

### -param dwRangeIndex [in]

A starting index inside the text recognition results for a recognized text range. This value should be between 0 and the range count.

### -param pszActionId [in]

Pointer to the identifier of the action to perform. This parameter cannot be set to <b>NULL</b>.

## -returns

Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.

## -remarks

The application must precede the call to <b>MappingDoAction</b> with a call to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>.

<div class="alert"><b>Warning</b>  The data referred to by the <i>pszText</i> and <i>pOptions</i> arguments passed to <a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a> 

must remain valid until the property bag structure passed by <i>pBag</i> is freed via 

<a href="/windows/desktop/api/elscore/nf-elscore-mappingfreepropertybag">MappingFreePropertyBag</a>. This is because both synchronous and asynchronous calls to 

<b>MappingRecognizeText</b> and <b>MappingDoAction</b> will attempt to use the data passed to the initial 

call to <b>MappingRecognizeText</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/extended-linguistic-services">Extended Linguistic Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services-functions">Extended Linguistic Services Functions</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_property_bag">MAPPING_PROPERTY_BAG</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappingrecognizetext">MappingRecognizeText</a>