---
UID: NE:http._HTTP_FEATURE_ID
title: HTTP_FEATURE_ID
description: Defines constants that specify an identifier for an HTTP feature.
ms.date: 09/28/2020
tech.root: http
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: http.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - _HTTP_FEATURE_ID
 - PHTTP_FEATURE_ID
 - HTTP_FEATURE_ID
f1_keywords:
 - _HTTP_FEATURE_ID
 - http/_HTTP_FEATURE_ID
 - PHTTP_FEATURE_ID
 - http/PHTTP_FEATURE_ID
 - HTTP_FEATURE_ID
 - http/HTTP_FEATURE_ID
dev_langs:
 - c++
---

## -description

Defines constants that specify an identifier for an HTTP feature.

## -enum-fields

### -field HttpFeatureUnknown:0

Specifies an unknown feature.

### -field HttpFeatureResponseTrailers:1

Specifies HTTP response trailers.

### -field HttpFeatureApiTimings:2

Specifies HTTP API timings.

### -field HttpFeatureDelegateEx:3

Specifies a request for delegation.

### -field HttpFeaturemax:0xFFFFFFFF

Specifies the maximum number of supported features.

## -remarks

## -see-also
