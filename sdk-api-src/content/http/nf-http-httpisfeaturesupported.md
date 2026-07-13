---
UID: NF:http.HttpIsFeatureSupported
title: HttpIsFeatureSupported
description: Checks whether a particular feature is supported.
ms.date: 09/28/2020
tech.root: http
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: http.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: httpapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - HttpIsFeatureSupported
f1_keywords:
 - HttpIsFeatureSupported
 - http/HttpIsFeatureSupported
dev_langs:
 - c++
---

## -description

Checks whether a particular feature is supported.

## -parameters

### -param FeatureId

Type: \_In\_ **[HTTP_FEATURE_ID](./ne-http-http_feature_id.md)**

The identifier of the feature.

## -returns

`TRUE` if the feature is supported, otherwise `FALSE`.

## -remarks

## -see-also
