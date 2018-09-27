---
UID: NS:strmif._VMRALPHABITMAP
title: "_VMRALPHABITMAP"
author: windows-sdk-content
description: The VMRALPHABITMAP structure is used in the VMR-7 filter's IVMRMixerBitmap methods when the application is providing a static alpha-blended bitmap to be displayed on the composited video frame.
old-location: dshow\vmralphabitmap.htm
tech.root: DirectShow
ms.assetid: 03b3e619-4804-42de-88d5-5422089e875a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PVMRALPHABITMAP, PVMRALPHABITMAP, PVMRALPHABITMAP structure pointer [DirectShow], VMRALPHABITMAP, VMRALPHABITMAP structure [DirectShow], VMRALPHABITMAPStructure, VMRBITMAP_DISABLE, VMRBITMAP_ENTIREDDS, VMRBITMAP_HDC, VMRBITMAP_SRCCOLORKEY, VMRBITMAP_SRCRECT, _VMRALPHABITMAP, dshow.vmralphabitmap, strmif/PVMRALPHABITMAP, strmif/VMRALPHABITMAP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRALPHABITMAP
product: Windows
targetos: Windows
req.typenames: VMRALPHABITMAP, *PVMRALPHABITMAP
req.redist: 
---

# _VMRALPHABITMAP structure


## -description


The <b>VMRALPHABITMAP</b> structure is used in the VMR-7 filter's <a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap</a> methods when the application is providing a static alpha-blended bitmap to be displayed on the composited video frame.
        


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

This flag is only valid for the  <a href="https://msdn.microsoft.com/039cb675-c384-4909-b06d-b331cc281df6">IVMRMixerBitmap::UpdateAlphaBitmapParameters</a> method. For the <a href="https://msdn.microsoft.com/92e57c3a-6761-4a54-83f5-0ea0ce80d60b">IVMRMixerBitmap::SetAlphaBitmap</a> method, the <b>rSrc</b> member must refer to the entire bitmap.

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




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

