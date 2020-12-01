---
UID: NS:d2d1effectauthor.D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
title: D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS (d2d1effectauthor.h)
description: Describes compute shader support, which is an option on D3D10 feature level.
helpviewer_keywords: ["D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS","D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure [Direct2D]","d2d1effectauthor/D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS","direct2d.d2d1__feature_data_d3d10_x_hardware_options"]
old-location: direct2d\d2d1__feature_data_d3d10_x_hardware_options.htm
tech.root: Direct2D
ms.assetid: 30EF82D6-7165-4DB7-B6F0-4EA72AA6987A
ms.date: 12/05/2018
ms.keywords: D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS, D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure [Direct2D], d2d1effectauthor/D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS, direct2d.d2d1__feature_data_d3d10_x_hardware_options
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
req.typenames: D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
 - d2d1effectauthor/D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
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
 - D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
---

# D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure


## -description

Describes compute shader support, which is an option on D3D10 feature level.

## -struct-fields

### -field computeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x

Shader model 4 compute shaders are supported.

## -remarks

You can fill this structure by passing a D2D1_ FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure to <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport">ID2D1EffectContext::CheckFeatureSupport</a>.