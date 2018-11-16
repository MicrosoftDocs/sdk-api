---
UID: NS:d2d1effectauthor.D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
title: D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
author: windows-sdk-content
description: Describes compute shader support, which is an option on D3D10 feature level.
old-location: direct2d\d2d1__feature_data_d3d10_x_hardware_options.htm
tech.root: Direct2D
ms.assetid: 30EF82D6-7165-4DB7-B6F0-4EA72AA6987A
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS, D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure [Direct2D], d2d1effectauthor/D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS, direct2d.d2d1__feature_data_d3d10_x_hardware_options
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS
req.redist: 
---

# D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure


## -description


Describes compute shader support, which is an option on D3D10 feature level.


## -struct-fields




### -field computeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x

Shader model 4 compute shaders are supported.


## -remarks



You can fill this structure by passing a D2D1_ FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure to <a href="https://msdn.microsoft.com/1A97B928-7715-4D4E-AD38-7D01EE243494">ID2D1EffectContext::CheckFeatureSupport</a>.



