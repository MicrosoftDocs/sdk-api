---
UID: NE:dxgi1_6.DXGI_ADAPTER_FLAG3
title: DXGI_ADAPTER_FLAG3 (dxgi1_6.h)
description: Identifies the type of DXGI adapter.
helpviewer_keywords: ["DXGI_ADAPTER_FLAG3","DXGI_ADAPTER_FLAG3 enumeration [DXGI]","DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE","DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE","DXGI_ADAPTER_FLAG3_NONE","DXGI_ADAPTER_FLAG3_REMOTE","DXGI_ADAPTER_FLAG3_SOFTWARE","DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES","DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES","DXGI_ADAPTER_FLAG_FORCE_DWORD","direct3ddxgi.DXGI_ADAPTER_FLAG3","dxgi1_6/DXGI_ADAPTER_FLAG3","dxgi1_6/DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE","dxgi1_6/DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE","dxgi1_6/DXGI_ADAPTER_FLAG3_NONE","dxgi1_6/DXGI_ADAPTER_FLAG3_REMOTE","dxgi1_6/DXGI_ADAPTER_FLAG3_SOFTWARE","dxgi1_6/DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES","dxgi1_6/DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES","dxgi1_6/DXGI_ADAPTER_FLAG_FORCE_DWORD"]
old-location: direct3ddxgi\DXGI_ADAPTER_FLAG3.htm
tech.root: direct3ddxgi
ms.assetid: 3CD83EEB-2F13-4B32-9E27-CF8456FB3E39
ms.date: 12/05/2018
ms.keywords: DXGI_ADAPTER_FLAG3, DXGI_ADAPTER_FLAG3 enumeration [DXGI], DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE, DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE, DXGI_ADAPTER_FLAG3_NONE, DXGI_ADAPTER_FLAG3_REMOTE, DXGI_ADAPTER_FLAG3_SOFTWARE, DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES, DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES, DXGI_ADAPTER_FLAG_FORCE_DWORD, direct3ddxgi.DXGI_ADAPTER_FLAG3, dxgi1_6/DXGI_ADAPTER_FLAG3, dxgi1_6/DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE, dxgi1_6/DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE, dxgi1_6/DXGI_ADAPTER_FLAG3_NONE, dxgi1_6/DXGI_ADAPTER_FLAG3_REMOTE, dxgi1_6/DXGI_ADAPTER_FLAG3_SOFTWARE, dxgi1_6/DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES, dxgi1_6/DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES, dxgi1_6/DXGI_ADAPTER_FLAG_FORCE_DWORD
req.header: dxgi1_6.h
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
req.typenames: DXGI_ADAPTER_FLAG3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_ADAPTER_FLAG3
 - dxgi1_6/DXGI_ADAPTER_FLAG3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_6.h
api_name:
 - DXGI_ADAPTER_FLAG3
---

## -description

Identifies the type of DXGI adapter.

## -enum-fields

### -field DXGI_ADAPTER_FLAG3_NONE:0

Specifies no flags.

### -field DXGI_ADAPTER_FLAG3_REMOTE:1

Value always set to 0. This flag is reserved.

### -field DXGI_ADAPTER_FLAG3_SOFTWARE:2

Specifies a software adapter. For more info about this flag, see <a href="/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi">new info in Windows 8 about enumerating adapters</a>.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.

### -field DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE:4

Specifies that the adapter's driver has been confirmed to work in an OS process where Arbitrary Code Guard (ACG) is enabled (i.e. dynamic code generation is disallowed).

### -field DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES:8

Specifies that the adapter supports monitored fences. These adapters support the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device::CreateFence</a> and <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5">ID3D11Device5::CreateFence</a> functions.

### -field DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES:0x10

Specifies that the adapter supports non-monitored fences. These adapters support the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device::CreateFence</a> function together with the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_fence_flags">D3D12_FENCE_FLAG_NON_MONITORED</a> flag.

<div class="alert"><b>Note</b>  For adapters that support both monitored and non-monitored fences, non-monitored fences are only supported when created with the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_fence_flags">D3D12_FENCE_FLAG_SHARED</a> and <b>D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER</b> flags. Monitored fences should always be used by supporting adapters unless communicating with an adapter that only supports non-monitored fences.</div>
<div> </div>

### -field DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE:0x20

Specifies that the adapter claims keyed mutex conformance. This signals a stronger guarantee that the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex">IDXGIKeyedMutex</a> interface behaves correctly.

### -field DXGI_ADAPTER_FLAG3_FORCE_DWORD:0xffffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -remarks

The <b>DXGI_ADAPTER_FLAG3</b> enumerated type is used by the <b>Flags</b> member of the <a href="/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3">DXGI_ADAPTER_DESC3</a> structure to ientify the type of DXGI adapter.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
