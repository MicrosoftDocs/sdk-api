---
UID: NE:d3d11.D3D11_FORMAT_SUPPORT2
title: D3D11_FORMAT_SUPPORT2 (d3d11.h)
description: Unordered resource support options for a compute shader resource (see ID3D11Device::CheckFeatureSupport).
helpviewer_keywords: ["560bc969-3791-be4b-1df7-1bec05505739","D3D11_FORMAT_SUPPORT2","D3D11_FORMAT_SUPPORT2 enumeration [Direct3D 11]","D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY","D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP","D3D11_FORMAT_SUPPORT2_SHAREABLE","D3D11_FORMAT_SUPPORT2_TILED","D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD","D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS","D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE","D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE","D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX","D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX","D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD","D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE","d3d11/D3D11_FORMAT_SUPPORT2","d3d11/D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY","d3d11/D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP","d3d11/D3D11_FORMAT_SUPPORT2_SHAREABLE","d3d11/D3D11_FORMAT_SUPPORT2_TILED","d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD","d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS","d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE","d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE","d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX","d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX","d3d11/D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD","d3d11/D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE","direct3d11.d3d11_format_support2"]
old-location: direct3d11\d3d11_format_support2.htm
tech.root: direct3d11
ms.assetid: 40650aae-ec0d-4c44-8abd-32c00343b717
ms.date: 12/05/2018
ms.keywords: 560bc969-3791-be4b-1df7-1bec05505739, D3D11_FORMAT_SUPPORT2, D3D11_FORMAT_SUPPORT2 enumeration [Direct3D 11], D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY, D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP, D3D11_FORMAT_SUPPORT2_SHAREABLE, D3D11_FORMAT_SUPPORT2_TILED, D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD, D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS, D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE, D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE, D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX, D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX, D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD, D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE, d3d11/D3D11_FORMAT_SUPPORT2, d3d11/D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY, d3d11/D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP, d3d11/D3D11_FORMAT_SUPPORT2_SHAREABLE, d3d11/D3D11_FORMAT_SUPPORT2_TILED, d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD, d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS, d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE, d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE, d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX, d3d11/D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX, d3d11/D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD, d3d11/D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE, direct3d11.d3d11_format_support2
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
req.typenames: D3D11_FORMAT_SUPPORT2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FORMAT_SUPPORT2
 - d3d11/D3D11_FORMAT_SUPPORT2
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
 - D3D11_FORMAT_SUPPORT2
---

# D3D11_FORMAT_SUPPORT2 enumeration


## -description

Unordered resource support options for a compute shader resource (see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a>).

## -enum-fields

### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD:0x1

Format supports atomic add.

### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS:0x2

Format supports atomic bitwise operations.

### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE:0x4

Format supports atomic compare with store or exchange.

### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE:0x8

Format supports atomic exchange.

### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX:0x10

Format supports atomic min and max.

### -field D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX:0x20

Format supports atomic unsigned min and max.

### -field D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD:0x40

Format supports a typed load.

### -field D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE:0x80

Format supports a typed store.

### -field D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP:0x100

Format supports logic operations in blend state.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.

### -field D3D11_FORMAT_SUPPORT2_TILED:0x200

Format supports tiled resources.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.

### -field D3D11_FORMAT_SUPPORT2_SHAREABLE:0x400

Format supports shareable resources.
              <div class="alert"><b>Note</b>  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R8G8B8A8_UNORM</a> and <b>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</b> are never shareable when using feature level 9, even if the device indicates optional feature support for <b>D3D11_FORMAT_SUPPORT_SHAREABLE</b>.
                Attempting to create shared resources with DXGI formats <b>DXGI_FORMAT_R8G8B8A8_UNORM</b> and <b>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</b> will always fail unless the feature level is 10_0 or higher.
              </div>
<div> </div>


<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.2.

### -field D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY:0x4000

Format supports multi-plane overlays.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
