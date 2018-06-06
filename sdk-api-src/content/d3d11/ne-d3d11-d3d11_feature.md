---
UID: NE:d3d11.D3D11_FEATURE
title: D3D11_FEATURE
author: windows-sdk-content
description: Direct3D 11 feature options.
old-location: direct3d11\d3d11_feature.htm
old-project: direct3d11
ms.assetid: 48c3bf65-f077-45e6-a306-03d5760eeccb
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D11_FEATURE, D3D11_FEATURE enumeration [Direct3D 11], D3D11_FEATURE_ARCHITECTURE_INFO, D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS, D3D11_FEATURE_D3D11_OPTIONS, D3D11_FEATURE_D3D11_OPTIONS1, D3D11_FEATURE_D3D11_OPTIONS2, D3D11_FEATURE_D3D11_OPTIONS3, D3D11_FEATURE_D3D11_OPTIONS4, D3D11_FEATURE_D3D9_OPTIONS, D3D11_FEATURE_D3D9_OPTIONS1, D3D11_FEATURE_D3D9_SHADOW_SUPPORT, D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT, D3D11_FEATURE_DOUBLES, D3D11_FEATURE_FORMAT_SUPPORT, D3D11_FEATURE_FORMAT_SUPPORT2, D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, D3D11_FEATURE_MARKER_SUPPORT, D3D11_FEATURE_SHADER_CACHE, D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT, D3D11_FEATURE_THREADING, d3d11/D3D11_FEATURE, d3d11/D3D11_FEATURE_ARCHITECTURE_INFO, d3d11/D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS, d3d11/D3D11_FEATURE_D3D11_OPTIONS, d3d11/D3D11_FEATURE_D3D11_OPTIONS1, d3d11/D3D11_FEATURE_D3D11_OPTIONS2, d3d11/D3D11_FEATURE_D3D11_OPTIONS3, d3d11/D3D11_FEATURE_D3D11_OPTIONS4, d3d11/D3D11_FEATURE_D3D9_OPTIONS, d3d11/D3D11_FEATURE_D3D9_OPTIONS1, d3d11/D3D11_FEATURE_D3D9_SHADOW_SUPPORT, d3d11/D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT, d3d11/D3D11_FEATURE_DOUBLES, d3d11/D3D11_FEATURE_FORMAT_SUPPORT, d3d11/D3D11_FEATURE_FORMAT_SUPPORT2, d3d11/D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT, d3d11/D3D11_FEATURE_MARKER_SUPPORT, d3d11/D3D11_FEATURE_SHADER_CACHE, d3d11/D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT, d3d11/D3D11_FEATURE_THREADING, direct3d11.d3d11_feature, f0675a94-9721-1d35-a01a-535e5c64006d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: D3D11_FEATURE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_FEATURE enumeration


## -description


Direct3D 11 feature options.


## -enum-fields




### -field D3D11_FEATURE_THREADING


            The driver supports <a href="https://msdn.microsoft.com/b4bef1e4-8d34-455c-8aed-01af974c66c8">multithreading</a>.
            To see an example of testing a driver for multithread support, see <a href="https://msdn.microsoft.com/f577357c-c2e5-4e58-9870-2e995bdc6782">How To: Check for Driver Support</a>.
           Refer to <a href="https://msdn.microsoft.com/1ad7d4c4-9da2-42b0-a461-e514060e3005">D3D11_FEATURE_DATA_THREADING</a>.


### -field D3D11_FEATURE_DOUBLES

Supports the use of the double-precision shaders in HLSL. Refer to <a href="https://msdn.microsoft.com/3cd4006b-25bd-46b8-9fa7-6b7d7eb82a75">D3D11_FEATURE_DATA_DOUBLES</a>.


### -field D3D11_FEATURE_FORMAT_SUPPORT


            Supports the formats in <a href="https://msdn.microsoft.com/8c7f62fd-e0fe-4f4d-8c88-ccf1372842f9">D3D11_FORMAT_SUPPORT</a>.
          Refer to <a href="https://msdn.microsoft.com/153e246e-9e2f-4557-94c4-a9f1a3b926bd">D3D11_FEATURE_DATA_FORMAT_SUPPORT</a>.


### -field D3D11_FEATURE_FORMAT_SUPPORT2


            Supports the formats in <a href="https://msdn.microsoft.com/40650aae-ec0d-4c44-8abd-32c00343b717">D3D11_FORMAT_SUPPORT2</a>.
          Refer to <a href="https://msdn.microsoft.com/075cc44a-3c91-4015-af7f-489b3b3c6661">D3D11_FEATURE_DATA_FORMAT_SUPPORT2</a>.


### -field D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS

Supports compute shaders and raw and structured buffers. Refer to <a href="https://msdn.microsoft.com/d41d1d78-21c1-4373-b579-6e051d6e8929">D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</a>.


### -field D3D11_FEATURE_D3D11_OPTIONS

Supports Direct3D 11.1 feature options. Refer to <a href="https://msdn.microsoft.com/02A3B423-75AB-4F44-BEBE-B8039EF384DC">D3D11_FEATURE_DATA_D3D11_OPTIONS</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FEATURE_ARCHITECTURE_INFO

Supports specific adapter architecture. Refer to <a href="https://msdn.microsoft.com/BC815FDB-984C-4857-AF48-8B471F46CDD4">D3D11_FEATURE_DATA_ARCHITECTURE_INFO</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FEATURE_D3D9_OPTIONS


              Supports Direct3D 9 feature options.
            Refer to <a href="https://msdn.microsoft.com/E5262261-28D7-4F7A-AB9A-A73FEADAE8FD">D3D11_FEATURE_DATA_D3D9_OPTIONS</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT


              Supports minimum precision of shaders.
              For more info about HLSL minimum precision, see <a href="direct3d_11_1_features.htm">using HLSL minimum precision</a>.
            Refer to <a href="https://msdn.microsoft.com/4494A896-E73E-4A41-BC73-F9BD49510276">D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FEATURE_D3D9_SHADOW_SUPPORT


              Supports Direct3D 9 shadowing feature. Refer to <a href="https://msdn.microsoft.com/E30500A0-D77D-4783-A5D5-418770DA1376">D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


### -field D3D11_FEATURE_D3D11_OPTIONS1

Supports Direct3D 11.2 feature options. Refer to <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.


### -field D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT

Supports Direct3D 11.2 instancing options. Refer to <a href="https://msdn.microsoft.com/940381BB-E8F6-416D-8F36-CC3591E70703">D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.


### -field D3D11_FEATURE_MARKER_SUPPORT

Supports Direct3D 11.2 marker options. Refer to <a href="https://msdn.microsoft.com/950381BB-E8F6-416D-8F36-CC3591E71703">D3D11_FEATURE_DATA_MARKER_SUPPORT</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.


### -field D3D11_FEATURE_D3D9_OPTIONS1


              Supports Direct3D 9 feature options, which includes the Direct3D 9 shadowing feature and instancing support. Refer to 
            <a href="https://msdn.microsoft.com/4894B4FC-1E95-42B1-B92D-E3B484ABDC74">D3D11_FEATURE_DATA_D3D9_OPTIONS1</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.


### -field D3D11_FEATURE_D3D11_OPTIONS2


              Supports Direct3D 11.3 conservative rasterization feature options.
            Refer to <a href="https://msdn.microsoft.com/D0CD9245-D8BC-48E5-A69B-0DB9B87E56A4">D3D11_FEATURE_DATA_D3D11_OPTIONS2</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.3.


### -field D3D11_FEATURE_D3D11_OPTIONS3


              Supports Direct3D 11.4 conservative rasterization feature options.
            Refer to <a href="https://msdn.microsoft.com/A8F9AAF5-F1C6-476D-AF14-5BCDEEDAF810">D3D11_FEATURE_DATA_D3D11_OPTIONS3</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.4.


### -field D3D11_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT


            Supports GPU virtual addresses. Refer to <a href="https://msdn.microsoft.com/662D9B07-755C-430D-84C6-B1E8876E26B5">D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a>.


### -field D3D11_FEATURE_D3D11_OPTIONS4


              Supports a single boolean for NV12 shared textures. Refer to <a href="https://msdn.microsoft.com/BC0DD66C-3452-440D-87EA-1504EFF89E3F">D3D11_FEATURE_DATA_D3D11_OPTIONS4</a>.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.4.


### -field D3D11_FEATURE_SHADER_CACHE

Supports shader cache, described in <a href="https://msdn.microsoft.com/45F1184E-0E82-4AF4-86F7-ED0E4C860026">D3D11_FEATURE_DATA_SHADER_CACHE</a>.


### -field D3D11_FEATURE_D3D11_OPTIONS5




## -remarks




          This enumeration is used when querying a driver about support for these features by calling <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a>.
          Each value in this enumeration has a corresponding data structure that is required to be passed to the <i>pFeatureSupportData</i> parameter
          of <b>ID3D11Device::CheckFeatureSupport</b>.
        




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

