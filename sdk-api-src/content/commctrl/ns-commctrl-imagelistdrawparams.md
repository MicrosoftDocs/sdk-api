---
UID: NS:commctrl._IMAGELISTDRAWPARAMS
title: IMAGELISTDRAWPARAMS (commctrl.h)
description: The IMAGELISTDRAWPARAMS structure contains information about an image list draw operation and is used with the IImageList::Draw function. 
helpviewer_keywords: ["*LPIMAGELISTDRAWPARAMS","BLACKNESS","CLR_DEFAULT","CLR_NONE","DSTINVERT","IMAGELISTDRAWPARAMS","IMAGELISTDRAWPARAMS structure [Windows Controls]","MERGECOPY","MERGEPAINT","NOTSRCCOPY","NOTSRCERASE","PATCOPY","PATINVERT","PATPAINT","SRCAND","SRCCOPY","SRCERASE","SRCINVERT","SRCPAINT","WHITENESS","_win32_IMAGELISTDRAWPARAMS","_win32_IMAGELISTDRAWPARAMS_cpp","commoncontrols/IMAGELISTDRAWPARAMS","controls.IMAGELISTDRAWPARAMS","controls._win32_IMAGELISTDRAWPARAMS"]
old-location: controls\IMAGELISTDRAWPARAMS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\structures\imagelistdrawparams.htm
ms.date: 08/02/2022
ms.keywords: '*LPIMAGELISTDRAWPARAMS, BLACKNESS, CLR_DEFAULT, CLR_NONE, DSTINVERT, IMAGELISTDRAWPARAMS, IMAGELISTDRAWPARAMS structure [Windows Controls], MERGECOPY, MERGEPAINT, NOTSRCCOPY, NOTSRCERASE, PATCOPY, PATINVERT, PATPAINT, SRCAND, SRCCOPY, SRCERASE, SRCINVERT, SRCPAINT, WHITENESS, _win32_IMAGELISTDRAWPARAMS, _win32_IMAGELISTDRAWPARAMS_cpp, commoncontrols/IMAGELISTDRAWPARAMS, controls.IMAGELISTDRAWPARAMS, controls._win32_IMAGELISTDRAWPARAMS'
req.header: commctrl.h
req.include-header: Commctrl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: IMAGELISTDRAWPARAMS, *LPIMAGELISTDRAWPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGELISTDRAWPARAMS
 - commctrl/_IMAGELISTDRAWPARAMS
 - LPIMAGELISTDRAWPARAMS
 - commctrl/LPIMAGELISTDRAWPARAMS
 - IMAGELISTDRAWPARAMS
 - commctrl/IMAGELISTDRAWPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - commoncontrols.h
api_name:
 - IMAGELISTDRAWPARAMS
---

# IMAGELISTDRAWPARAMS structure


## -description

Contains information about an image list draw operation and is used with the <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-draw">IImageList::Draw</a> function.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The size of this structure, in bytes.

### -field himl

Type: <b>HIMAGELIST</b>

A handle to the image list that contains the image to be drawn.

### -field i

Type: <b>int</b>

The zero-based index of the image to be drawn.

### -field hdcDst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

A handle to the destination device context.

### -field x

Type: <b>int</b>

The x-coordinate that specifies where the image is drawn.

### -field y

Type: <b>int</b>

The y-coordinate that specifies where the image is drawn.

### -field cx

Type: <b>int</b>

A value that specifies the number of pixels to draw, relative to the upper-left corner of the drawing operation as specified by <b>xBitmap</b> and <b>yBitmap</b>. If <b>cx</b> and <b>cy</b> are zero, then <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-draw">Draw</a> draws the entire valid section. The method does not ensure that the parameters are valid.

### -field cy

Type: <b>int</b>

A value that specifies the number of pixels to draw, relative to the upper-left corner of the drawing operation as specified by <b>xBitmap</b> and <b>yBitmap</b>. If <b>cx</b> and <b>cy</b> are zero, then <a href="/windows/desktop/api/commoncontrols/nf-commoncontrols-iimagelist-draw">Draw</a> draws the entire valid section. The method does not ensure that the parameters are valid.

### -field xBitmap

Type: <b>int</b>

The x-coordinate that specifies the upper-left corner of the drawing operation in reference to the image itself. Pixels of the image that are to the left of <b>xBitmap</b> and above <b>yBitmap</b> do not appear.

### -field yBitmap

Type: <b>int</b>

The y-coordinate that specifies the upper-left corner of the drawing operation in reference to the image itself. Pixels of the image that are to the left of <b>xBitmap</b> and above <b>yBitmap</b> do not appear.

### -field rgbBk

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The image background color. This parameter can be an application-defined RGB value or one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLR_DEFAULT"></a><a id="clr_default"></a><dl>
<dt><b>CLR_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The default background color. The image is drawn using the image list background color. 

</td>
</tr>
<tr>
<td width="40%"><a id="CLR_NONE"></a><a id="clr_none"></a><dl>
<dt><b>CLR_NONE</b></dt>
</dl>
</td>
<td width="60%">
No background color. The image is drawn transparently. 

</td>
</tr>
</table>

### -field rgbFg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The image foreground color. This member is used only if <b>fStyle</b> includes the <a href="/windows/desktop/Controls/imagelistdrawflags">ILD_BLEND25</a> or <a href="/windows/desktop/Controls/imagelistdrawflags">ILD_BLEND50</a> flag. This parameter can be an application-defined RGB value or one of the following values:  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLR_DEFAULT"></a><a id="clr_default"></a><dl>
<dt><b>CLR_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The default foreground color. The image is drawn using the system highlight color as the foreground color. 

</td>
</tr>
<tr>
<td width="40%"><a id="CLR_NONE"></a><a id="clr_none"></a><dl>
<dt><b>CLR_NONE</b></dt>
</dl>
</td>
<td width="60%">
No blend color. The image is blended with the color of the destination device context. 

</td>
</tr>
</table>

### -field fStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A flag specifying the drawing style and, optionally, the overlay image. See the comments section at the end of this topic for information on the overlay image. This member can contain one or more <a href="/windows/desktop/Controls/imagelistdrawflags">image list drawing flags</a>.

### -field dwRop

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A value specifying a raster operation code. These codes define how the color data for the source rectangle will be combined with the color data for the destination rectangle to achieve the final color. This member is ignored if	<b>fStyle</b> does not include the <a href="/windows/desktop/Controls/imagelistdrawflags">ILD_ROP</a> flag. Some common raster operation codes include: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BLACKNESS"></a><a id="blackness"></a><dl>
<dt><b>BLACKNESS</b></dt>
</dl>
</td>
<td width="60%">
Fills the destination rectangle using the color associated with index zero in the physical palette. (This color is black for the default physical palette.) 

</td>
</tr>
<tr>
<td width="40%"><a id="DSTINVERT"></a><a id="dstinvert"></a><dl>
<dt><b>DSTINVERT</b></dt>
</dl>
</td>
<td width="60%">
Inverts the destination rectangle. 

</td>
</tr>
<tr>
<td width="40%"><a id="MERGECOPY"></a><a id="mergecopy"></a><dl>
<dt><b>MERGECOPY</b></dt>
</dl>
</td>
<td width="60%">
Merges the source rectangle colors with the specified pattern by using the Boolean <b>AND</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="MERGEPAINT"></a><a id="mergepaint"></a><dl>
<dt><b>MERGEPAINT</b></dt>
</dl>
</td>
<td width="60%">
Merges the inverted source rectangle colors with the destination rectangle colors by using the Boolean <b>OR</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="NOTSRCCOPY"></a><a id="notsrccopy"></a><dl>
<dt><b>NOTSRCCOPY</b></dt>
</dl>
</td>
<td width="60%">
Copies the inverted source rectangle to the destination. 

</td>
</tr>
<tr>
<td width="40%"><a id="NOTSRCERASE"></a><a id="notsrcerase"></a><dl>
<dt><b>NOTSRCERASE</b></dt>
</dl>
</td>
<td width="60%">
Combines the source and destination rectangle colors by using the Boolean <b>OR</b> operator. Inverts the resultant color. 

</td>
</tr>
<tr>
<td width="40%"><a id="PATCOPY"></a><a id="patcopy"></a><dl>
<dt><b>PATCOPY</b></dt>
</dl>
</td>
<td width="60%">
Copies the specified pattern into the destination bitmap. 

</td>
</tr>
<tr>
<td width="40%"><a id="PATINVERT"></a><a id="patinvert"></a><dl>
<dt><b>PATINVERT</b></dt>
</dl>
</td>
<td width="60%">
Combines the specified pattern colors with the destination rectangle colors by using the Boolean <b>XOR</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="PATPAINT"></a><a id="patpaint"></a><dl>
<dt><b>PATPAINT</b></dt>
</dl>
</td>
<td width="60%">
Combines the pattern colors with the inverted source rectangle colors and combines the result with the destination rectangle colors by using the Boolean <b>OR</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="SRCAND"></a><a id="srcand"></a><dl>
<dt><b>SRCAND</b></dt>
</dl>
</td>
<td width="60%">
Combines the source and destination rectangle colors by using the Boolean <b>AND</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="SRCCOPY"></a><a id="srccopy"></a><dl>
<dt><b>SRCCOPY</b></dt>
</dl>
</td>
<td width="60%">
Copies the source rectangle directly to the destination rectangle. 

</td>
</tr>
<tr>
<td width="40%"><a id="SRCERASE"></a><a id="srcerase"></a><dl>
<dt><b>SRCERASE</b></dt>
</dl>
</td>
<td width="60%">
Combines the destination rectangle's inverted colors with the source rectangle colors by using the Boolean <b>AND</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="SRCINVERT"></a><a id="srcinvert"></a><dl>
<dt><b>SRCINVERT</b></dt>
</dl>
</td>
<td width="60%">
Combines the source and destination rectangle colors by using the Boolean <b>XOR</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="SRCPAINT"></a><a id="srcpaint"></a><dl>
<dt><b>SRCPAINT</b></dt>
</dl>
</td>
<td width="60%">
Combines the source and destination rectangle colors by using the Boolean <b>OR</b> operator. 

</td>
</tr>
<tr>
<td width="40%"><a id="WHITENESS"></a><a id="whiteness"></a><dl>
<dt><b>WHITENESS</b></dt>
</dl>
</td>
<td width="60%">
Fills the destination rectangle using the color associated with index one in the physical palette. This color is white for the default physical palette. 

</td>
</tr>
</table>

### -field fState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A flag that specifies the drawing state. This member can contain one or more <a href="/windows/desktop/Controls/imageliststateflags">image list state flags</a>. You must use comctl32.dll version 6 to use this member. See the Remarks.

### -field Frame

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Used with the <b>alpha blending</b> effect.

When used with <a href="/windows/desktop/Controls/imageliststateflags">ILS_ALPHA</a>, this member holds the value for the alpha channel. This value can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque. 

You must use comctl32.dll version 6 to use this member. See the Remarks.

### -field crEffect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A color used for the <b>glow</b> and <b>shadow</b> effects. You must use comctl32.dll version 6 to use this member. See the Remarks.

## -remarks

An overlay image is an image that is drawn on top of the primary image specified in the <b>i</b> member of this structure. To specify an overlay image, use the bitwise <b>OR</b> operator to combine <b>fStyle</b> with the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a> macro, passing the one-based index of the overlay image in the macro. This image must have been previously specified as an overlay image using the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_setoverlayimage">ImageList_SetOverlayImage</a> API. 

To extract the overlay image from the <b>fStyle</b>, use the bitwise <b>AND</b> operator to mask <b>fStyle</b> with the <a href="/windows/desktop/Controls/imagelistdrawflags">ILD_OVERLAYMASK</a> value. 

Comctl32.dll version 6 is not redistributable. To use Comctl32.dll version 6, you must specify it in a manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
