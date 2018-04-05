---
UID: NS:d3d9types._D3DINDEXBUFFER_DESC
title: "_D3DINDEXBUFFER_DESC"
author: windows-driver-content
description: Describes an index buffer.
old-location: direct3d9\d3dindexbuffer_desc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dindexbuffer_desc.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 44abff56-0c27-c3fa-b5c1-778c9f24dee9, D3DINDEXBUFFER_DESC, D3DINDEXBUFFER_DESC structure [Direct3D 9], D3DUSAGE_DONOTCLIP, D3DUSAGE_DYNAMIC, D3DUSAGE_NPATCHES, D3DUSAGE_POINTS, D3DUSAGE_RTPATCHES, D3DUSAGE_SOFTWAREPROCESSING, D3DUSAGE_WRITEONLY, LPD3DINDEXBUFFER_DESC, LPD3DINDEXBUFFER_DESC structure pointer [Direct3D 9], _D3DINDEXBUFFER_DESC, d3d9types/D3DINDEXBUFFER_DESC, d3d9types/LPD3DINDEXBUFFER_DESC, direct3d9.d3dindexbuffer_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DINDEXBUFFER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DINDEXBUFFER_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DINDEXBUFFER_DESC structure


## -description


Describes an index buffer.


## -struct-fields




### -field Format

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the surface format of the index buffer data.


### -field Type

Type: <b><a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a> enumerated type, identifying this resource as an index buffer.


### -field Usage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more of the following flags, specifying the usage for this resource.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3DUSAGE_DONOTCLIP"></a><a id="d3dusage_donotclip"></a><dl>
<dt><b>D3DUSAGE_DONOTCLIP</b></dt>
</dl>
</td>
<td width="60%">
Set to indicate that the index buffer content will never require clipping.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DUSAGE_DYNAMIC"></a><a id="d3dusage_dynamic"></a><dl>
<dt><b>D3DUSAGE_DYNAMIC</b></dt>
</dl>
</td>
<td width="60%">
Set to indicate that the index buffer requires dynamic memory use. This is useful for drivers because it enables them to decide where to place the buffer. In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory. Note that there is no separate static usage; if you do not specify D3DUSAGE_DYNAMIC the index buffer is made static. D3DUSAGE_DYNAMIC is strictly enforced through the D3DLOCK_DISCARD and D3DLOCK_NOOVERWRITE locking flags. As a result, D3DLOCK_DISCARD and D3DLOCK_NOOVERWRITE are only valid on index buffers created with D3DUSAGE_DYNAMIC; they are not valid flags on static vertex buffers.

For more information about using dynamic index buffers, see <a href="https://msdn.microsoft.com/074f848e-4a42-48a2-adf7-4026b8967413">Using Dynamic Vertex and Index Buffers</a>.

Note that D3DUSAGE_DYNAMIC cannot be specified on managed index buffers. For more information, see <a href="https://msdn.microsoft.com/4aa55313-b86c-48e7-829a-a0917c2ebae7">Managing Resources (Direct3D 9)</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DUSAGE_RTPATCHES"></a><a id="d3dusage_rtpatches"></a><dl>
<dt><b>D3DUSAGE_RTPATCHES</b></dt>
</dl>
</td>
<td width="60%">
Set to indicate when the index buffer is to be used for drawing high-order primitives.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DUSAGE_NPATCHES"></a><a id="d3dusage_npatches"></a><dl>
<dt><b>D3DUSAGE_NPATCHES</b></dt>
</dl>
</td>
<td width="60%">
Set to indicate when the index buffer is to be used for drawing N patches.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DUSAGE_POINTS"></a><a id="d3dusage_points"></a><dl>
<dt><b>D3DUSAGE_POINTS</b></dt>
</dl>
</td>
<td width="60%">
Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DUSAGE_SOFTWAREPROCESSING"></a><a id="d3dusage_softwareprocessing"></a><dl>
<dt><b>D3DUSAGE_SOFTWAREPROCESSING</b></dt>
</dl>
</td>
<td width="60%">
Set to indicate that the buffer is to be used with software processing.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DUSAGE_WRITEONLY"></a><a id="d3dusage_writeonly"></a><dl>
<dt><b>D3DUSAGE_WRITEONLY</b></dt>
</dl>
</td>
<td width="60%">
Informs the system that the application writes only to the index buffer. Using this flag enables the driver to choose the best memory location for efficient write operations and rendering. Attempts to read from an index buffer that is created with this capability can result in degraded performance.

</td>
</tr>
</table>
 


### -field Pool

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Member of the <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a> enumerated type, specifying the class of memory allocated for this index buffer.


### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the index buffer, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/33c33c28-b57a-4e52-a29b-9117bd60460b">GetDesc</a>



<a href="https://msdn.microsoft.com/baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784">Index Buffers (Direct3D 9)</a>
 

 

