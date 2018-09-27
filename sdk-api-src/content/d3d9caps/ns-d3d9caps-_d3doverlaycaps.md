---
UID: NS:d3d9caps._D3DOVERLAYCAPS
title: "_D3DOVERLAYCAPS"
author: windows-sdk-content
description: Specifies hardware overlay capabilities for a Direct3D device.
old-location: mf\d3doverlaycaps.htm
tech.root: medfound
ms.assetid: 4d9e031d-af01-4b8a-b90c-9d83b09c24da
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: D3DOVERLAYCAPS, D3DOVERLAYCAPS structure [Media Foundation], D3DOVERLAYCAPS_FULLRANGERGB, D3DOVERLAYCAPS_LIMITEDRANGERGB, D3DOVERLAYCAPS_STRETCHX, D3DOVERLAYCAPS_STRETCHY, D3DOVERLAYCAPS_YCbCr_BT601, D3DOVERLAYCAPS_YCbCr_BT601_xvYCC, D3DOVERLAYCAPS_YCbCr_BT709, D3DOVERLAYCAPS_YCbCr_BT709_xvYCC, _D3DOVERLAYCAPS, d3d9caps/D3DOVERLAYCAPS, mf.d3doverlaycaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d9caps.h
req.include-header: D3d9.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d9caps.h
api_name:
 - D3DOVERLAYCAPS
product: Windows
targetos: Windows
req.typenames: D3DOVERLAYCAPS
req.redist: 
---

# _D3DOVERLAYCAPS structure


## -description


Specifies hardware overlay capabilities for a Direct3D device.


## -struct-fields




### -field Caps

Contains a bitwise <b>OR</b> of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_FULLRANGERGB"></a><a id="d3doverlaycaps_fullrangergb"></a><dl>
<dt><b>D3DOVERLAYCAPS_FULLRANGERGB</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The overlay supports RGB with a nominal range of 0–255 per channel.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_LIMITEDRANGERGB"></a><a id="d3doverlaycaps_limitedrangergb"></a><dl>
<dt><b>D3DOVERLAYCAPS_LIMITEDRANGERGB</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The overlay supports RGB with a nominal range of 16–235 per channel. Reference black is (16,16,16) and reference white is (235,235,235).

</td>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_YCbCr_BT601"></a><a id="d3doverlaycaps_ycbcr_bt601"></a><a id="D3DOVERLAYCAPS_YCBCR_BT601"></a><dl>
<dt><b>D3DOVERLAYCAPS_YCbCr_BT601</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The overlay supports the BT.601 definition of YUV.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_YCbCr_BT709"></a><a id="d3doverlaycaps_ycbcr_bt709"></a><a id="D3DOVERLAYCAPS_YCBCR_BT709"></a><dl>
<dt><b>D3DOVERLAYCAPS_YCbCr_BT709</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The overlay supports the BT.709 definition of YUV.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_YCbCr_BT601_xvYCC"></a><a id="d3doverlaycaps_ycbcr_bt601_xvycc"></a><a id="D3DOVERLAYCAPS_YCBCR_BT601_XVYCC"></a><dl>
<dt><b>D3DOVERLAYCAPS_YCbCr_BT601_xvYCC</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The overlay supports extended YCbCr (xvYCC) for BT.601 YUV.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_YCbCr_BT709_xvYCC"></a><a id="d3doverlaycaps_ycbcr_bt709_xvycc"></a><a id="D3DOVERLAYCAPS_YCBCR_BT709_XVYCC"></a><dl>
<dt><b>D3DOVERLAYCAPS_YCbCr_BT709_xvYCC</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The overlay supports extended YCbCr (xvYCC) for BT.709 YUV.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_STRETCHX"></a><a id="d3doverlaycaps_stretchx"></a><dl>
<dt><b>D3DOVERLAYCAPS_STRETCHX</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The device can stretch and shrink the overlay data arbitrarily in the horizontal direction.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DOVERLAYCAPS_STRETCHY"></a><a id="d3doverlaycaps_stretchy"></a><dl>
<dt><b>D3DOVERLAYCAPS_STRETCHY</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The device can stretch and shrink the overlay data arbitrarily in the vertical direction.

</td>
</tr>
</table>
 


### -field MaxOverlayDisplayWidth

The maximum overlay width after stretching.


### -field MaxOverlayDisplayHeight

The maximum overlay height after stretching.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/83880b6f-f8a0-4be4-a400-ea86ca41f9e7">IDirect3D9ExOverlayExtension::CheckDeviceOverlayType</a>
 

 

