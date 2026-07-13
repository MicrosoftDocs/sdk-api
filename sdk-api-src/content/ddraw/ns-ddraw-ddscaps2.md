---
UID: NS:ddraw._DDSCAPS2
title: DDSCAPS2
description: The DDSCAPS2 structure defines additional capabilities of a Microsoft DirectDraw surface object.
tech.root: directdraw
ms.date: 07/11/2022
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ddraw.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DDSCAPS2
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ddraw.h
api_name:
 - _DDSCAPS2
 - DDSCAPS2
f1_keywords:
 - _DDSCAPS2
 - ddraw/_DDSCAPS2
 - DDSCAPS2
 - ddraw/DDSCAPS2
dev_langs:
 - c++
helpviewer_keywords:
 - _DDSCAPS2
---

## -description

The DDSCAPS2 structure defines additional capabilities of a Microsoft DirectDraw surface object.

## -struct-fields

### -field dwCaps

Specifies a set of flags representing the capabilities of the surface. The flags in this member are identical to those in the corresponding member of the [**DDSCAPS**](ns-ddraw-ddscaps.md) structure.

### -field dwCaps2

Specifies a set of flags that indicate additional surface capabilities. This member can contain one or more of the following capability flags. Each of these flags, except DDSCAPS2\_TEXTUREMANAGE, are set by the application when the application calls its **CreateSurface** method.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flag</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DDSCAPS2_ADDITIONALPRIMARY</p></td>
<td><p><strong>Microsoft DirectX 9.0 and later versions only.</strong></p>
<p>Indicates that subordinate heads of a multiple-head card are no longer in control of their video memory after surfaces are created for those subordinate heads with this bit set. Once such surfaces are destroyed, subordinate heads regain control of their memory. For more information, see <a href="/windows-hardware/drivers/display/managing-multiple-head-memory">Managing Multiple-Head Memory</a>.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_COMMANDBUFFER</p></td>
<td><p>Marks a command buffer, used by Microsoft Direct3D to batch commands.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_CUBEMAP</p></td>
<td><p>This surface is a cubic environment map. When using this flag, also specify the face or faces of the cubic environment map to create.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_CUBEMAP_POSITIVEX</p></td>
<td><p>This flag is used with the DDSCAPS2_CUBEMAP flag to create the positive X face of a cubic environment map.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_CUBEMAP_NEGATIVEX</p></td>
<td><p>This flag is used with the DDSCAPS2_CUBEMAP flag to create the negative X face of a cubic environment map.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_CUBEMAP_POSITIVEY</p></td>
<td><p>This flag is used with the DDSCAPS2_CUBEMAP flag to create the positive Y face of a cubic environment map.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_CUBEMAP_NEGATIVEY</p></td>
<td><p>This flag is used with the DDSCAPS2_CUBEMAP flag to create the negative Y face of a cubic environment map.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_CUBEMAP_POSITIVEZ</p></td>
<td><p>This flag is used with the DDSCAPS2_CUBEMAP flag to create the positive Z face of a cubic environment map.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_CUBEMAP_NEGATIVEZ</p></td>
<td><p>This flag is used with the DDSCAPS2_CUBEMAP flag to create the negative Z face of a cubic environment map.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_CUBEMAP_ALLFACES</p></td>
<td><p>This flag is used with the DDSCAPS2_CUBEMAP flag to create all six faces of a cubic environment map.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_D3DTEXTUREMANAGE</p></td>
<td><p>The texture is always managed by Direct3D.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_DISCARDBACKBUFFER</p></td>
<td><p><strong>DirectX 8.0 and later versions only.</strong></p>
<p></p>
Indicates that preservation of the back buffer is not required. It will be set on the primary surface and the back buffers if the application has set D3DSWAPEFFECT_DISCARD on the Present API.
<strong>DirectX 9.0 and later versions only.</strong>
Indicates that preservation of the depth-stencil surface is not required.</td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_DONOTPERSIST</p></td>
<td><p>The managed surface can be safely lost.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_ENABLEALPHACHANNEL</p></td>
<td><p><strong>DirectX 8.1 and later versions only.</strong></p>
<p>Indicates to create surfaces that are part of a primary flipping chain or that are on stand-alone back buffers. This flag turns on the alpha channel. For more information, see <a href="/windows-hardware/drivers/display/enabling-alpha-channels-on-full-screen-back-buffers">Enabling Alpha Channels On Full-Screen Back Buffers</a>.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_EXTENDEDFORMATPRIMARY</p></td>
<td><p><strong>DirectX 9.0 and later versions only.</strong></p>
<p>Indicates to create a dummy primary surface for use with a nonstandard display mode. For more information, see <a href="/windows-hardware/drivers/display/switching-between-standard-and-nonstandard-modes">Switching Between Standard and Nonstandard Modes</a>.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_HARDWAREDEINTERLACE</p></td>
<td><p>The driver must convert the interlaced signal to progressive frames. The DDSCAPS_VIDEOPORT and DDSCAPS_OVERLAY flags in this structure must also be set.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_HINTANTIALIASING</p></td>
<td><p>The application will use antialiasing. This flag is valid only if the DDSCAPS_3DDEVICE flag is also set.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_HINTDYNAMIC</p></td>
<td><p>The application will be updating the surface frequently. Surfaces with this flag set must also have the DDSCAPS_TEXTURE flag in this structure set. This flag cannot be used with the DDSCAPS2_HINTSTATIC or DDSCAPS2_OPAQUE flags.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_HINTSTATIC</p></td>
<td><p>The application will be updating the surface infrequently, but still requires access. Surfaces with this flag set must also have the DDSCAPS_TEXTURE flag in this structure set. This flag cannot be used with the DDSCAPS2_HINTDYNAMIC or DDSCAPS2_OPAQUE flags.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_INDEXBUFFER</p></td>
<td><p><strong>DirectX 8.0 and later versions only.</strong></p>
<p>Marks an index buffer, created and controlled by the application.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_MIPMAPSUBLEVEL</p></td>
<td><p>It enables easier use of <strong>GetAttachedSurface</strong>, rather than <strong>EnumAttachedSurfaces</strong>, for surface constructs such as cube maps, in which there is more than one mipmap surface attached to the root surface. This should be set on all nontop-level surfaces in a mipmapped cube map so that a call to <strong>GetAttachedSurface</strong> can distinguish between top-level faces and attached mipmap levels. This capability bit is ignored by <strong>CreateSurface</strong>.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_NOTUSERLOCKABLE</p></td>
<td><p><strong>DirectX 8.0 and later versions only.</strong></p>
<p></p>
Set on the primary and the back buffers if the flipping chain is not lockable, or on any render target that is not lockable. This allows drivers to do behind the scenes optimization. Note that it is still possible to lock the surfaces so the driver must handle these cases, but such locks are infrequent and are not expected to be fast.
The driver can also determine whether the depth/stencil buffer is lockable by the presence of this flag.</td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_NPATCHES</p></td>
<td><p><strong>DirectX 8.0 and later versions only.</strong></p>
<p>Indicates that the vertex buffer data can be used to render n-patches.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_OPAQUE</p></td>
<td><p>The application will never lock, blit, or update the surface for the rest of that surface's lifetime. The driver can compress or reorder the surface without ever having to decompress it. Surfaces with this flag set must also have the DDSCAPS_TEXTURE flag in this structure set. This flag cannot be used with the DDSCAPS2_HINTDYNAMIC or DDSCAPS2_HINTSTATIC flags.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_POINTS</p></td>
<td><p><strong>DirectX 8.0 and later versions only.</strong></p>
<p>Indicates that the vertex buffer data can be used to render points and point sprites.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_RTPATCHES</p></td>
<td><p><strong>DirectX 8.0 and later versions only.</strong></p>
<p>Indicates that the vertex buffer data can be used to render rt-patches.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_STEREOSURFACELEFT</p></td>
<td><p>This surface is part of a stereo flipping chain. When this flag is set during a <strong>CreateSurface</strong> call, a pair of stereo surfaces are created for each buffer in the primary flipping chain. You must create a complex flipping chain (with back buffers). You cannot create a single set of stereo surfaces. The <strong>Flip</strong> method requires back buffers, so at least 4 surfaces must be created.</p>
<p>In addition, when this flag is set in a <a href="ns-ddraw-ddsurfacedesc.md"><strong>DDSURFACEDESC</strong></a> structure as the result of an <strong>EnumDisplayModes</strong> or <strong>GetDisplayMode</strong> call, it indicates support for stereo in that mode.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_TEXTUREMANAGE</p></td>
<td><p>The client indicates that this texture surface should be managed by the driver if possible; otherwise it is managed by Direct3D Immediate Mode. This flag can be used only for texture surfaces (DDSCAPS_TEXTURE flag set in the <strong>dwCaps</strong> member). For more information, see Automatic Texture Management in the Direct3D Immediate Mode documentation.</p></td>
</tr>
<tr class="odd">
<td><p>DDSCAPS2_VERTEXBUFFER</p></td>
<td><p>Marks an explicit vertex buffer, created and controlled by the application.</p></td>
</tr>
<tr class="even">
<td><p>DDSCAPS2_VOLUME</p></td>
<td><p><strong>DirectX 8.0 and later versions only.</strong></p>
<p>This flag is set if the texture has depth in addition to width and height.</p></td>
</tr>
</tbody>
</table>

### -field dwCaps3

**DirectX 8.0 and DirectX 8.1 versions only.**

Specifies the number of samples for a multisampled surface. This field holds one of the values of the enumerated type D3DMULTISAMPLE\_TYPE. If a surface is not multisampled, **dwCaps3** has the value D3DMULTISAMPLE\_NONE (0).

**DirectX 9.0 and later versions only.**

Specifies a set of bits that indicate additional surface capabilities. This member can be a bitwise OR of the following bits.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Bits</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Bits in the DDSCAPS3_MULTISAMPLE_MASK mask (0x0000001FL).</p></td>
<td><p>The first five bits of <strong>dwCaps3</strong> indicate the number of samples for a multiple-sampled surface. The number of samples can be specified using one of the values of the enumerated type D3DMULTISAMPLE_TYPE. If a surface is not multisampled, this value is D3DMULTISAMPLE_NONE (0).</p></td>
</tr>
<tr class="even">
<td><p>Bits in the DDSCAPS3_MULTISAMPLE_QUALITY_MASK mask (0x000000E0L).</p></td>
<td><p></p>
The next three bits of <strong>dwCaps3</strong> indicate the quality level of rendering samples in a multiple-sampled surface. The quality level must be a number from 0 to 7 that represents a quality level from 1 to 8 respectively.
Note that even if a surface is not multisampled (specified in the first five bits using D3DMULTISAMPLE_NONE) it can still have a greater-than-1 quality level (specified using a number greater than 0).</td>
</tr>
<tr class="odd">
<td><p></p>
DDSCAPS3_RESERVED1
(0x00000100L)</td>
<td><p>Reserved</p></td>
</tr>
<tr class="even">
<td><p></p>
DDSCAPS3_VIDEO
(0x00000200L)</td>
<td><p></p>
Indicates that the render target contains video data.
Note that several render targets can be created with this flag, and if two or more of these render targets belong to the same Direct3D context, then the driver determines that these render targets all display the same video stream regardless of whether the render target surfaces are attached to each other.</td>
</tr>
<tr class="odd">
<td><p></p>
DDSCAPS3_LIGHTWEIGHTMIPMAP
(0x00000400L)</td>
<td><p>Indicates whether this surface has lightweight mip levels</p></td>
</tr>
<tr class="even">
<td><p></p>
DDSCAPS3_AUTOGENMIPMAP
(0x00000800L)</td>
<td><p>Indicates that the mip sublevels for this surface are automatically generated.</p></td>
</tr>
<tr class="odd">
<td><p></p>
DDSCAPS3_DMAP
(0x00001000L)</td>
<td><p>Indicates a displacement-map texture that can be sampled by the displacement-map sampler in the tessellation unit.</p></td>
</tr>
</tbody>
</table>

### -field DUMMYUNIONNAMEN

N/A

### -field DUMMYUNIONNAMEN.dwCaps4

The low word is the depth for a volume texture.

### -field DUMMYUNIONNAMEN.dwVolumeDepth

Specifies the volume texture bit-depth.

## -remarks

This structure is used by the driver to report the types of surfaces the driver supports. It is also filled in by an application to specify the type of surface to be created.

## -see-also
