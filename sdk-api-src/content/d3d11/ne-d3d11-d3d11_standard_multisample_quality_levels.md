---
UID: NE:d3d11.D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS
title: D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS (d3d11.h)
description: Specifies a multi-sample pattern type.
helpviewer_keywords: ["D3D11_CENTER_MULTISAMPLE_PATTERN","D3D11_STANDARD_MULTISAMPLE_PATTERN","D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS","D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS enumeration [Direct3D 11]","d3d11/D3D11_CENTER_MULTISAMPLE_PATTERN","d3d11/D3D11_STANDARD_MULTISAMPLE_PATTERN","d3d11/D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS","direct3d11.d3d11_standard_multisample_quality_levels","fb0a6e23-49e9-934e-53e2-2a05f3e76371"]
old-location: direct3d11\d3d11_standard_multisample_quality_levels.htm
tech.root: direct3d11
ms.assetid: 20c558ae-e9c3-4bab-8c11-264d626f2cff
ms.date: 12/05/2018
ms.keywords: D3D11_CENTER_MULTISAMPLE_PATTERN, D3D11_STANDARD_MULTISAMPLE_PATTERN, D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS, D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS enumeration [Direct3D 11], d3d11/D3D11_CENTER_MULTISAMPLE_PATTERN, d3d11/D3D11_STANDARD_MULTISAMPLE_PATTERN, d3d11/D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS, direct3d11.d3d11_standard_multisample_quality_levels, fb0a6e23-49e9-934e-53e2-2a05f3e76371
req.header: d3d11.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS
 - d3d11/D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS
---

# D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS enumeration


## -description

Specifies a multi-sample pattern type.

## -enum-fields

### -field D3D11_STANDARD_MULTISAMPLE_PATTERN:0xffffffff

Pre-defined multi-sample patterns required for Direct3D 11 and Direct3D 10.1 hardware.

### -field D3D11_CENTER_MULTISAMPLE_PATTERN:0xfffffffe

Pattern where all of the samples are located at the pixel center.

## -remarks

An app calls <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkmultisamplequalitylevels">ID3D11Device::CheckMultisampleQualityLevels</a> to get the number of quality levels available during multisampling. A 0 quality level means the hardware does not support multisampling for the particular format. If the number of quality levels is greater than 0 and the hardware supports the fixed sample patterns for the sample count, the app can request the fixed patterns by specifying quality level as either <b>D3D11_STANDARD_MULTISAMPLE_PATTERN</b> or <b>D3D11_CENTER_MULTISAMPLE_PATTERN</b>. The app can call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport">ID3D11Device::CheckFormatSupport</a> to check for support of the standard fixed patterns. If the hardware only supports the fixed patterns but no additional vendor-specific patterns, the runtime can report the number of quality levels as 1, and the hardware can pretend 0 quality level behaves the same as quality level equal to D3D11_STANDARD_MULTISAMPLE_PATTERN.

The runtime defines the following standard sample patterns for 1(trivial),  2, 4, 8, and 16 sample counts. Hardware must support 1, 4, and 8 sample counts. Hardware vendors can expose more sample counts beyond these. However, if vendors support 2, 4(required), 8(required), or 16, they must also support the corresponding standard pattern or center pattern for each of those sample counts.

<img alt="Pattern for 1 Sample Count" src="./images/D3D11_MSAAGrid.png"/>

<img alt="Patterns for 2 and 4 Sample Count" src="./images/D3D11_MSAAPatterns_2_4.png"/>

<img alt="Patterns for 8 and 16 Sample Count" src="./images/D3D11_MSAAPatterns_8_16.png"/>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
