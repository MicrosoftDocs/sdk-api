---
UID: NF:d2d1_3.ID2D1TransformedImageSource.GetProperties
title: ID2D1TransformedImageSource::GetProperties (d2d1_3.h)
description: Retrieves the properties specified when the transformed image source was created.
helpviewer_keywords: ["GetProperties","GetProperties method [Direct2D]","GetProperties method [Direct2D]","ID2D1TransformedImageSource interface","ID2D1TransformedImageSource interface [Direct2D]","GetProperties method","ID2D1TransformedImageSource.GetProperties","ID2D1TransformedImageSource::GetProperties","d2d1_3/ID2D1TransformedImageSource::GetProperties","direct2d.id2d1transformedimagesource_getproperties"]
old-location: direct2d\id2d1transformedimagesource_getproperties.htm
tech.root: Direct2D
ms.assetid: D8291B02-9C32-412B-8F25-63A4A551B023
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [Direct2D], GetProperties method [Direct2D],ID2D1TransformedImageSource interface, ID2D1TransformedImageSource interface [Direct2D],GetProperties method, ID2D1TransformedImageSource.GetProperties, ID2D1TransformedImageSource::GetProperties, d2d1_3/ID2D1TransformedImageSource::GetProperties, direct2d.id2d1transformedimagesource_getproperties
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: D2D1.lib
req.dll: D2D1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1TransformedImageSource::GetProperties
 - d2d1_3/ID2D1TransformedImageSource::GetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.dll
api_name:
 - ID2D1TransformedImageSource.GetProperties
---

# ID2D1TransformedImageSource::GetProperties


## -description

Retrieves the properties specified when the transformed image source was created.
        This value corresponds to the value passed to <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createtransformedimagesource">CreateTransformedImageSource</a>.

## -parameters

### -param properties [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties">D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES</a>*</b>

the properties specified when the transformed image source was created.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1transformedimagesource">ID2D1TransformedImageSource</a>