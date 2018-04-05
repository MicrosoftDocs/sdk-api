---
UID: NS:d3d9types._D3DCLIPSTATUS9
title: "_D3DCLIPSTATUS9"
author: windows-driver-content
description: Describes the current clip status.
old-location: direct3d9\d3dclipstatus9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dclipstatus9.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DCLIPSTATUS9, D3DCLIPSTATUS9 structure [Direct3D 9], D3DCS_ALL, D3DCS_BACK, D3DCS_BOTTOM, D3DCS_FRONT, D3DCS_LEFT, D3DCS_PLANE0, D3DCS_PLANE1, D3DCS_PLANE2, D3DCS_PLANE3, D3DCS_PLANE4, D3DCS_PLANE5, D3DCS_RIGHT, D3DCS_TOP, LPD3DCLIPSTATUS9, LPD3DCLIPSTATUS9 structure pointer [Direct3D 9], _D3DCLIPSTATUS9, c1b8b346-7ca8-121f-0471-08d17d5b4691, d3d9types/D3DCLIPSTATUS9, d3d9types/LPD3DCLIPSTATUS9, direct3d9.d3dclipstatus9
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
req.typenames: D3DCLIPSTATUS9
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DCLIPSTATUS9
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DCLIPSTATUS9 structure


## -description


Describes the current clip status.


## -struct-fields




### -field ClipUnion

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Clip union flags that describe the current clip status. This member can be one or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3DCS_ALL"></a><a id="d3dcs_all"></a><dl>
<dt><b>D3DCS_ALL</b></dt>
</dl>
</td>
<td width="60%">
Combination of all clip flags.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_LEFT"></a><a id="d3dcs_left"></a><dl>
<dt><b>D3DCS_LEFT</b></dt>
</dl>
</td>
<td width="60%">
All vertices are clipped by the left plane of the viewing frustum.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_RIGHT"></a><a id="d3dcs_right"></a><dl>
<dt><b>D3DCS_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
All vertices are clipped by the right plane of the viewing frustum.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_TOP"></a><a id="d3dcs_top"></a><dl>
<dt><b>D3DCS_TOP</b></dt>
</dl>
</td>
<td width="60%">
All vertices are clipped by the top plane of the viewing frustum.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_BOTTOM"></a><a id="d3dcs_bottom"></a><dl>
<dt><b>D3DCS_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
All vertices are clipped by the bottom plane of the viewing frustum.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_FRONT"></a><a id="d3dcs_front"></a><dl>
<dt><b>D3DCS_FRONT</b></dt>
</dl>
</td>
<td width="60%">
All vertices are clipped by the front plane of the viewing frustum.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_BACK"></a><a id="d3dcs_back"></a><dl>
<dt><b>D3DCS_BACK</b></dt>
</dl>
</td>
<td width="60%">
All vertices are clipped by the back plane of the viewing frustum.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_PLANE0"></a><a id="d3dcs_plane0"></a><dl>
<dt><b>D3DCS_PLANE0</b></dt>
</dl>
</td>
<td width="60%">
Application-defined clipping planes.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_PLANE1"></a><a id="d3dcs_plane1"></a><dl>
<dt><b>D3DCS_PLANE1</b></dt>
</dl>
</td>
<td width="60%">
Application-defined clipping planes.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_PLANE2"></a><a id="d3dcs_plane2"></a><dl>
<dt><b>D3DCS_PLANE2</b></dt>
</dl>
</td>
<td width="60%">
Application-defined clipping planes.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_PLANE3"></a><a id="d3dcs_plane3"></a><dl>
<dt><b>D3DCS_PLANE3</b></dt>
</dl>
</td>
<td width="60%">
Application-defined clipping planes.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_PLANE4"></a><a id="d3dcs_plane4"></a><dl>
<dt><b>D3DCS_PLANE4</b></dt>
</dl>
</td>
<td width="60%">
Application-defined clipping planes.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCS_PLANE5"></a><a id="d3dcs_plane5"></a><dl>
<dt><b>D3DCS_PLANE5</b></dt>
</dl>
</td>
<td width="60%">
Application-defined clipping planes.

</td>
</tr>
</table>
 


### -field ClipIntersection

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Clip intersection flags that describe the current clip status. This member can take the same flags as ClipUnion. 


## -remarks



When clipping is enabled during vertex processing (by <a href="https://msdn.microsoft.com/0a34ecb6-6437-46dc-aa79-bf4d24395a86">ProcessVertices</a>, <a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">DrawPrimitive</a>, or other drawing functions), Direct3D computes a clip code for every vertex. The clip code is a combination of D3DCS_* bits. When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code. Direct3D maintains the clip status using <b>D3DCLIPSTATUS9</b>, which has ClipUnion and ClipIntersection members. ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes. Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection. When D3DRS_CLIPPING is set to <b>FALSE</b>, ClipUnion and ClipIntersection are set to zero. Direct3D updates the clip status during drawing calls. To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.


    
    Clip status is not updated by <a href="https://msdn.microsoft.com/478b4a3d-3366-47ec-8a66-92aa2aa06477">DrawRectPatch</a> and <a href="https://msdn.microsoft.com/9076fbe6-0f14-4b28-8f34-145e4eac6f22">DrawTriPatch</a> because there is no software emulation for them.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>



<a href="https://msdn.microsoft.com/b8a68504-bc0f-4d36-a3f4-729fa9ab5004">GetClipStatus</a>



<a href="https://msdn.microsoft.com/c035c2a3-79e3-4e33-a3d5-7674ba3cda88">SetClipStatus</a>
 

 

