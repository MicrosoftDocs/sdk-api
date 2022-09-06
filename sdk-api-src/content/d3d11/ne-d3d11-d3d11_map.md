---
UID: NE:d3d11.D3D11_MAP
title: D3D11_MAP (d3d11.h)
description: Identifies a resource to be accessed for reading and writing by the CPU. Applications may combine one or more of these flags.
helpviewer_keywords: ["8c057b75-49d4-723a-fe77-d236c5e87682","D3D11_MAP","D3D11_MAP enumeration [Direct3D 11]","D3D11_MAP_READ","D3D11_MAP_READ_WRITE","D3D11_MAP_WRITE","D3D11_MAP_WRITE_DISCARD","D3D11_MAP_WRITE_NO_OVERWRITE","d3d11/D3D11_MAP","d3d11/D3D11_MAP_READ","d3d11/D3D11_MAP_READ_WRITE","d3d11/D3D11_MAP_WRITE","d3d11/D3D11_MAP_WRITE_DISCARD","d3d11/D3D11_MAP_WRITE_NO_OVERWRITE","direct3d11.d3d11_map"]
old-location: direct3d11\d3d11_map.htm
tech.root: direct3d11
ms.assetid: 916b00bd-2711-4ebd-a36d-d75b3a59a528
ms.date: 12/05/2018
ms.keywords: 8c057b75-49d4-723a-fe77-d236c5e87682, D3D11_MAP, D3D11_MAP enumeration [Direct3D 11], D3D11_MAP_READ, D3D11_MAP_READ_WRITE, D3D11_MAP_WRITE, D3D11_MAP_WRITE_DISCARD, D3D11_MAP_WRITE_NO_OVERWRITE, d3d11/D3D11_MAP, d3d11/D3D11_MAP_READ, d3d11/D3D11_MAP_READ_WRITE, d3d11/D3D11_MAP_WRITE, d3d11/D3D11_MAP_WRITE_DISCARD, d3d11/D3D11_MAP_WRITE_NO_OVERWRITE, direct3d11.d3d11_map
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
req.typenames: D3D11_MAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_MAP
 - d3d11/D3D11_MAP
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
 - D3D11_MAP
---

# D3D11_MAP enumeration


## -description

Identifies a resource to be accessed for reading and writing by the CPU. Applications may combine one or more of these flags.

## -enum-fields

### -field D3D11_MAP_READ:1

Resource is mapped for reading. The resource must have been created with read access 
      (see <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_READ</a>).

### -field D3D11_MAP_WRITE:2

Resource is mapped for writing. The resource must have been created with write 
      access (see <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_WRITE</a>).

### -field D3D11_MAP_READ_WRITE:3

Resource is mapped for reading and writing. The resource must have been created with read and write 
      access (see <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_READ and D3D11_CPU_ACCESS_WRITE</a>).

### -field D3D11_MAP_WRITE_DISCARD:4

Resource is mapped for writing; the previous contents of the resource will be undefined. The resource must have been created with write access 
      and dynamic usage (See <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_WRITE</a> and <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DYNAMIC</a>).

### -field D3D11_MAP_WRITE_NO_OVERWRITE:5

Resource is mapped for writing; the existing contents of the resource cannot be overwritten (see Remarks). This flag is only valid on vertex and 
      index buffers. The resource must have been created with write access (see <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_WRITE</a>). 
      Cannot be used on a resource created with the <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_CONSTANT_BUFFER</a> flag.

<div class="alert"><b>Note</b>  The Direct3D 11.1 runtime, which is available starting with Windows 8, enables  mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_map">D3D11_MAP_WRITE_NO_OVERWRITE</a>.  The Direct3D 11 and earlier runtimes limited mapping to vertex or index buffers. To determine if a Direct3D device supports these features, call <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a> with <a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE_D3D11_OPTIONS</a>. <b>CheckFeatureSupport</b> fills members of a <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options">D3D11_FEATURE_DATA_D3D11_OPTIONS</a> structure with the device's features. The relevant members here are <b>MapNoOverwriteOnDynamicConstantBuffer</b> and <b>MapNoOverwriteOnDynamicBufferSRV</b>.</div>
<div> </div>

## -remarks

This enumeration is used in <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a>.

<h3><a id="NO_OVERWRITE_DETAILS"></a><a id="no_overwrite_details"></a>Meaning of D3D11_MAP_WRITE_NO_OVERWRITE</h3>
<b>D3D11_MAP_WRITE_NO_OVERWRITE</b> signifies that the application promises not to write to data that the input assembler (IA) stage is using. In exchange, the GPU allows the application to write to other parts of the same buffer.  The application must ensure that it does not write over any data in use by the IA stage.

For example, consider the buffer illustrated in the following diagram. If a <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-draw">Draw</a> call has been issued that uses vertices 4-6, then an application that calls <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map">Map</a> on this buffer must ensure that it does not write to the vertices that the <b>Draw</b> call will access during rendering.

<img alt="Diagram of a buffer that includes vertices in different stages of utilization" src="./images/D3D10_map_nooverwrite.png"/>
However, ensuring this can be difficult, because the GPU is often many frames behind the CPU in terms of which frame it is currently processing. Keeping track of which sections of a resource are being used because of calls made 2 to 5 frames ago is difficult and error-prone. Because of this, it is recommended that applications only write to the uninitialized portions of a resource when using <b>D3D11_MAP_WRITE_NO_OVERWRITE</b>.

<h3><a id="DISCARD_NO_OVERWRITE_USES"></a><a id="discard_no_overwrite_uses"></a>Common Usage of D3D11_MAP_WRITE_DISCARD with D3D11_MAP_WRITE_NO_OVERWRITE</h3>
<b>D3D11_MAP_WRITE_DISCARD</b> and <b>D3D11_MAP_WRITE_NO_OVERWRITE</b> are normally used in conjunction with dynamic index/vertex buffers. <b>D3D11_MAP_WRITE_DISCARD</b> can also be used with dynamic textures. However, <b>D3D11_MAP_WRITE_NO_OVERWRITE</b> cannot be used with dynamic textures.

A common use of these two flags involves filling dynamic index/vertex buffers with geometry that can be seen from the camera's current position. The first time that data is entered into the buffer on a given frame, <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map">Map</a> is called with <b>D3D11_MAP_WRITE_DISCARD</b>; doing so invalidates the previous contents of the buffer. The buffer is then filled with all available data.

Subsequent writes to the buffer within the same frame should use <b>D3D11_MAP_WRITE_NO_OVERWRITE</b>. This will enable the CPU to access a resource that is potentially being used by the GPU as long as the restrictions described previously are respected.

## -see-also

<a href="/windows/win32/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
