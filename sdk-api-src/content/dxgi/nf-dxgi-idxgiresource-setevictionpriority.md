---
UID: NF:dxgi.IDXGIResource.SetEvictionPriority
title: IDXGIResource::SetEvictionPriority (dxgi.h)
description: Set the priority for evicting the resource from memory.
helpviewer_keywords: ["27202bac-1045-b4a9-634f-9fe77668f2ab","DXGI_RESOURCE_PRIORITY_HIGH (0xa0000000)","DXGI_RESOURCE_PRIORITY_LOW (0x50000000)","DXGI_RESOURCE_PRIORITY_MAXIMUM (0xc8000000)","DXGI_RESOURCE_PRIORITY_MINIMUM (0x28000000)","DXGI_RESOURCE_PRIORITY_NORMAL (0x78000000)","IDXGIResource interface [DXGI]","SetEvictionPriority method","IDXGIResource.SetEvictionPriority","IDXGIResource::SetEvictionPriority","SetEvictionPriority","SetEvictionPriority method [DXGI]","SetEvictionPriority method [DXGI]","IDXGIResource interface","direct3ddxgi.idxgiresource_setevictionpriority","dxgi/IDXGIResource::SetEvictionPriority"]
old-location: direct3ddxgi\idxgiresource_setevictionpriority.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource_setevictionpriority.htm
ms.date: 12/05/2018
ms.keywords: 27202bac-1045-b4a9-634f-9fe77668f2ab, DXGI_RESOURCE_PRIORITY_HIGH (0xa0000000), DXGI_RESOURCE_PRIORITY_LOW (0x50000000), DXGI_RESOURCE_PRIORITY_MAXIMUM (0xc8000000), DXGI_RESOURCE_PRIORITY_MINIMUM (0x28000000), DXGI_RESOURCE_PRIORITY_NORMAL (0x78000000), IDXGIResource interface [DXGI],SetEvictionPriority method, IDXGIResource.SetEvictionPriority, IDXGIResource::SetEvictionPriority, SetEvictionPriority, SetEvictionPriority method [DXGI], SetEvictionPriority method [DXGI],IDXGIResource interface, direct3ddxgi.idxgiresource_setevictionpriority, dxgi/IDXGIResource::SetEvictionPriority
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIResource::SetEvictionPriority
 - dxgi/IDXGIResource::SetEvictionPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIResource.SetEvictionPriority
---

# IDXGIResource::SetEvictionPriority


## -description

Set the priority for evicting the resource from memory.

## -parameters

### -param EvictionPriority

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The priority is one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXGI_RESOURCE_PRIORITY_MINIMUM__0x28000000_"></a><a id="dxgi_resource_priority_minimum__0x28000000_"></a><a id="DXGI_RESOURCE_PRIORITY_MINIMUM__0X28000000_"></a><dl>
<dt><b>DXGI_RESOURCE_PRIORITY_MINIMUM (0x28000000)</b></dt>
</dl>
</td>
<td width="60%">
The resource is unused and can be evicted as soon as another resource requires the memory that the resource occupies.

</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_RESOURCE_PRIORITY_LOW__0x50000000_"></a><a id="dxgi_resource_priority_low__0x50000000_"></a><a id="DXGI_RESOURCE_PRIORITY_LOW__0X50000000_"></a><dl>
<dt><b>DXGI_RESOURCE_PRIORITY_LOW (0x50000000)</b></dt>
</dl>
</td>
<td width="60%">
The eviction priority of the resource is low. The placement of the resource is not critical, and minimal work is performed to find a location for the resource. For example, if a GPU can render with a vertex buffer from either local or non-local memory with little difference in performance, that vertex buffer is low priority. Other more critical resources (for example, a render target or texture) can then occupy the faster memory.

</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_RESOURCE_PRIORITY_NORMAL__0x78000000_"></a><a id="dxgi_resource_priority_normal__0x78000000_"></a><a id="DXGI_RESOURCE_PRIORITY_NORMAL__0X78000000_"></a><dl>
<dt><b>DXGI_RESOURCE_PRIORITY_NORMAL (0x78000000)</b></dt>
</dl>
</td>
<td width="60%">
The eviction priority of the resource is normal. The placement of the resource is important, but not critical, for performance. The resource is placed in its preferred location instead of a low-priority resource. 

</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_RESOURCE_PRIORITY_HIGH__0xa0000000_"></a><a id="dxgi_resource_priority_high__0xa0000000_"></a><a id="DXGI_RESOURCE_PRIORITY_HIGH__0XA0000000_"></a><dl>
<dt><b>DXGI_RESOURCE_PRIORITY_HIGH (0xa0000000)</b></dt>
</dl>
</td>
<td width="60%">
The eviction priority of the resource is high. The resource is placed in its preferred location instead of a low-priority or normal-priority resource.

</td>
</tr>
<tr>
<td width="40%"><a id="DXGI_RESOURCE_PRIORITY_MAXIMUM__0xc8000000_"></a><a id="dxgi_resource_priority_maximum__0xc8000000_"></a><a id="DXGI_RESOURCE_PRIORITY_MAXIMUM__0XC8000000_"></a><dl>
<dt><b>DXGI_RESOURCE_PRIORITY_MAXIMUM (0xc8000000)</b></dt>
</dl>
</td>
<td width="60%">
The resource is evicted from memory only if there is no other way of resolving the memory requirement.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

The eviction priority is a memory-management variable that is used by DXGI for determining how to populate overcommitted memory.

You can set priority levels other than the defined values when appropriate. For example, you can set a resource with a priority level of 0x78000001 to indicate that the resource is slightly above normal.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a>