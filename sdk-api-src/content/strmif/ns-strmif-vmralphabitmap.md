---
UID: NS:strmif._VMRALPHABITMAP
title: VMRALPHABITMAP (strmif.h)
description: The VMRALPHABITMAP structure is used in the VMR-7 filter's IVMRMixerBitmap methods when the application is providing a static alpha-blended bitmap to be displayed on the composited video frame.
helpviewer_keywords: ["*PVMRALPHABITMAP","PVMRALPHABITMAP","PVMRALPHABITMAP structure pointer [DirectShow]","VMRALPHABITMAP","VMRALPHABITMAP structure [DirectShow]","VMRALPHABITMAPStructure","VMRBITMAP_DISABLE","VMRBITMAP_ENTIREDDS","VMRBITMAP_HDC","VMRBITMAP_SRCCOLORKEY","VMRBITMAP_SRCRECT","dshow.vmralphabitmap","strmif/PVMRALPHABITMAP","strmif/VMRALPHABITMAP"]
old-location: dshow\vmralphabitmap.htm
tech.root: dshow
ms.assetid: 03b3e619-4804-42de-88d5-5422089e875a
ms.date: 4/26/2023
ms.keywords: '*PVMRALPHABITMAP, PVMRALPHABITMAP, PVMRALPHABITMAP structure pointer [DirectShow], VMRALPHABITMAP, VMRALPHABITMAP structure [DirectShow], VMRALPHABITMAPStructure, VMRBITMAP_DISABLE, VMRBITMAP_ENTIREDDS, VMRBITMAP_HDC, VMRBITMAP_SRCCOLORKEY, VMRBITMAP_SRCRECT, dshow.vmralphabitmap, strmif/PVMRALPHABITMAP, strmif/VMRALPHABITMAP'
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VMRALPHABITMAP, *PVMRALPHABITMAP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMRALPHABITMAP
 - strmif/_VMRALPHABITMAP
 - PVMRALPHABITMAP
 - strmif/PVMRALPHABITMAP
 - VMRALPHABITMAP
 - strmif/VMRALPHABITMAP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRALPHABITMAP
---

# VMRALPHABITMAP structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VMRALPHABITMAP</b> structure is used in the VMR-7 filter's <a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap</a> methods when the application is providing a static alpha-blended bitmap to be displayed on the composited video frame.

## -struct-fields

### -field dwFlags

Flags that instruct the mixer where to find the bitmap. The following values are defined.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VMRBITMAP_DISABLE"></a><a id="vmrbitmap_disable"></a><dl>
<dt><b>VMRBITMAP_DISABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Disable the bitmap. This flag cannot be combined with other flags.

</td>
</tr>
<tr>
<td width="40%"><a id="VMRBITMAP_HDC"></a><a id="vmrbitmap_hdc"></a><dl>
<dt><b>VMRBITMAP_HDC</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Obtain the bitmap from the HDC. If this flag is set, the <b>hdc</b> member must specify a valid handle to a device context, and the <b>pDDS</b> member must be <b>NULL</b>.

If this flag is absent, the <b>pDDS</b> member must point to a valid DirectDraw surface, and the <b>hdc</b> member must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VMRBITMAP_ENTIREDDS"></a><a id="vmrbitmap_entiredds"></a><dl>
<dt><b>VMRBITMAP_ENTIREDDS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Take the entire DirectDraw surface. When this flag is specified, <b>rSrc</b> is ignored. This flag cannot be combined with the <b>VMRBITMAP_HDC</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="VMRBITMAP_SRCCOLORKEY"></a><a id="vmrbitmap_srccolorkey"></a><dl>
<dt><b>VMRBITMAP_SRCCOLORKEY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The <b>clrSrcKey</b> value is valid and should be used when blending.

</td>
</tr>
<tr>
<td width="40%"><a id="VMRBITMAP_SRCRECT"></a><a id="vmrbitmap_srcrect"></a><dl>
<dt><b>VMRBITMAP_SRCRECT</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>rSrc</b> rectangle is valid and specifies a sub-rectangle of the original app image to be blended. 

This flag is only valid for the  <a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters">IVMRMixerBitmap::UpdateAlphaBitmapParameters</a> method. For the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap">IVMRMixerBitmap::SetAlphaBitmap</a> method, the <b>rSrc</b> member must refer to the entire bitmap.

</td>
</tr>
</table>

### -field hdc

The handle to the device context for the bitmap. Specify <b>NULL</b> if the bitmap is located in a DirectDraw surface.

### -field pDDS

Pointer to a DirectDraw surface that contains the bitmap. Specify <b>NULL</b> if the bitmap is to be obtained from a GDI device context. If a DirectDraw surface is specified, 
          the pixel format must be ARGB-32 or RGB-32. If the surface contains per-pixel alpha, do not set the VMRBITMAP_SRCCOLORKEY flag in <b>dwFlags</b>.

### -field rSrc

Specifies the source rectangle in either the GDI device context or the DirectDraw surface.

### -field rDest

Specifies the destination rectangle in composition space.

### -field fAlpha

Specifies the alpha blending value; must be a value from 0.0 to 1.0 (inclusive).

### -field clrSrcKey

Specifies the source color key.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>