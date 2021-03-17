---
UID: NF:d3d11sdklayers.ID3D11RefDefaultTrackingOptions.SetTrackingOptions
title: ID3D11RefDefaultTrackingOptions::SetTrackingOptions (d3d11sdklayers.h)
description: Sets graphics processing unit (GPU) debug reference default tracking options for specific resource types.
helpviewer_keywords: ["ID3D11RefDefaultTrackingOptions interface [Direct3D 11]","SetTrackingOptions method","ID3D11RefDefaultTrackingOptions.SetTrackingOptions","ID3D11RefDefaultTrackingOptions::SetTrackingOptions","SetTrackingOptions","SetTrackingOptions method [Direct3D 11]","SetTrackingOptions method [Direct3D 11]","ID3D11RefDefaultTrackingOptions interface","d3d11sdklayers/ID3D11RefDefaultTrackingOptions::SetTrackingOptions","direct3d11.id3d11refdefaulttrackingoptions_settrackingoptions"]
old-location: direct3d11\id3d11refdefaulttrackingoptions_settrackingoptions.htm
tech.root: direct3d11
ms.assetid: A54AAC4C-CD38-4326-AF99-9FB74CC0A1A0
ms.date: 12/05/2018
ms.keywords: ID3D11RefDefaultTrackingOptions interface [Direct3D 11],SetTrackingOptions method, ID3D11RefDefaultTrackingOptions.SetTrackingOptions, ID3D11RefDefaultTrackingOptions::SetTrackingOptions, SetTrackingOptions, SetTrackingOptions method [Direct3D 11], SetTrackingOptions method [Direct3D 11],ID3D11RefDefaultTrackingOptions interface, d3d11sdklayers/ID3D11RefDefaultTrackingOptions::SetTrackingOptions, direct3d11.id3d11refdefaulttrackingoptions_settrackingoptions
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11RefDefaultTrackingOptions::SetTrackingOptions
 - d3d11sdklayers/ID3D11RefDefaultTrackingOptions::SetTrackingOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler.lib
 - D3DCompiler.dll
api_name:
 - ID3D11RefDefaultTrackingOptions.SetTrackingOptions
---

# ID3D11RefDefaultTrackingOptions::SetTrackingOptions


## -description

Sets graphics processing unit (GPU) debug reference default tracking options for specific resource types.

## -parameters

### -param ResourceTypeFlags

A <a href="/windows/desktop/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type">D3D11_SHADER_TRACKING_RESOURCE_TYPE</a>-typed value that specifies the type of resource to track.

### -param Options

A combination of <a href="/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options">D3D11_SHADER_TRACKING_OPTIONS</a>-typed flags that are combined by using a bitwise <b>OR</b> operation. The resulting value identifies tracking options. If a flag is present, the tracking option that the flag represents is set to "on"; otherwise the tracking option is set to "off."

## -returns

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions">ID3D11RefDefaultTrackingOptions</a>