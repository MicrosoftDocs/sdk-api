---
UID: NS:d2d1effectauthor.D2D1_FEATURE_DATA_DOUBLES
title: D2D1_FEATURE_DATA_DOUBLES (d2d1effectauthor.h)
description: Describes the support for doubles in shaders.
helpviewer_keywords: ["D2D1_FEATURE_DATA_DOUBLES","D2D1_FEATURE_DATA_DOUBLES structure [Direct2D]","d2d1effectauthor/D2D1_FEATURE_DATA_DOUBLES","direct2d.d2d1_feature_data_doubles"]
old-location: direct2d\d2d1_feature_data_doubles.htm
tech.root: Direct2D
ms.assetid: 29EDAD15-FFFF-4F0D-BB0D-B4BF37AC609F
ms.date: 12/05/2018
ms.keywords: D2D1_FEATURE_DATA_DOUBLES, D2D1_FEATURE_DATA_DOUBLES structure [Direct2D], d2d1effectauthor/D2D1_FEATURE_DATA_DOUBLES, direct2d.d2d1_feature_data_doubles
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_FEATURE_DATA_DOUBLES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FEATURE_DATA_DOUBLES
 - d2d1effectauthor/D2D1_FEATURE_DATA_DOUBLES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_FEATURE_DATA_DOUBLES
---

# D2D1_FEATURE_DATA_DOUBLES structure


## -description

Describes the support for doubles in shaders.

## -struct-fields

### -field doublePrecisionFloatShaderOps

TRUE is doubles are supported within the shaders.

## -remarks

Fill this structure by passing a D2D1_FEATURE_DOUBLES structure to <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport">ID2D1EffectContext::CheckFeatureSupport</a>.