---
UID: NL:gdiplusmetaheader.MetafileHeader
title: MetafileHeader (gdiplusmetaheader.h)
description: A MetafileHeader object stores properties of an associated metafile.
helpviewer_keywords: ["MetafileHeader","MetafileHeader class [GDI+]","MetafileHeader class [GDI+]","described","_gdiplus_CLASS_MetafileHeader_Class","gdiplus._gdiplus_CLASS_MetafileHeader_Class","gdiplusmetaheader/MetafileHeader"]
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheader.htm
ms.date: 12/05/2018
ms.keywords: MetafileHeader, MetafileHeader class [GDI+], MetafileHeader class [GDI+],described, _gdiplus_CLASS_MetafileHeader_Class, gdiplus._gdiplus_CLASS_MetafileHeader_Class, gdiplusmetaheader/MetafileHeader
req.header: gdiplusmetaheader.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MetafileHeader
 - gdiplusmetaheader/MetafileHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusmetaheader.h
api_name:
 - MetafileHeader
---

# MetafileHeader class


## -description

A <b>MetafileHeader</b> object stores properties of an associated metafile.

<b>MetafileHeader</b> has these types of members:
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getbounds">MetafileHeader::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getbounds">MetafileHeader::GetBounds</a> method gets the bounding rectangle for the associated metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getdpix">MetafileHeader::GetDpiX</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getdpix">MetafileHeader::GetDpiX</a> method gets the horizontal dots per inch of the associated metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getdpiy">MetafileHeader::GetDpiY</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getdpiy">MetafileHeader::GetDpiY</a> method gets the vertical dots per inch of the associated metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getemfheader">MetafileHeader::GetEmfHeader</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getemfheader">MetafileHeader::GetEmfHeader</a> method gets an <a href="/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-enhmetaheader3">ENHMETAHEADER3</a> structure that contains properties of the associated metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getemfplusflags">MetafileHeader::GetEmfPlusFlags</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getemfplusflags">MetafileHeader::GetEmfPlusFlags</a> method gets a flag that indicates whether the associated metafile was recorded against a video display device context.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getmetafilesize">MetafileHeader::GetMetafileSize</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getmetafilesize">MetafileHeader::GetMetafileSize</a> method gets the size, in bytes, of the metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-gettype">MetafileHeader::GetType</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-gettype">MetafileHeader::GetType</a> method gets the type of the associated metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getversion">MetafileHeader::GetVersion</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getversion">MetafileHeader::GetVersion</a> method gets the version of the metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getwmfheader">MetafileHeader::GetWmfHeader</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-getwmfheader">MetafileHeader::GetWmfHeader</a> method gets a <a href="/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a> structure that contains properties of the associated metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isdisplay">MetafileHeader::IsDisplay</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isdisplay">MetafileHeader::IsDisplay</a> method determines whether the associated metafile was recorded against a video display device context.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemf">MetafileHeader::IsEmf</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemf">MetafileHeader::IsEmf</a> method determines whether the associated metafile is in the EMF format.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemforemfplus">MetafileHeader::IsEmfOrEmfPlus</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemforemfplus">MetafileHeader::IsEmfOrEmfPlus</a> method determines whether the associated metafile is in either the EMF or EMF+ format.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemfplus">MetafileHeader::IsEmfPlus</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemfplus">MetafileHeader::IsEmfPlus</a> method determines whether the associated metafile is in the EMF+ format.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemfplusdual">MetafileHeader::IsEmfPlusDual</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemfplusdual">MetafileHeader::IsEmfPlusDual</a> method determines whether the associated metafile is in the EMF+ Dual format.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemfplusonly">MetafileHeader::IsEmfPlusOnly</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-isemfplusonly">MetafileHeader::IsEmfPlusOnly</a> method determines whether the associated metafile is in the EMF+ Only format.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-iswmf">MetafileHeader::IsWmf</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-iswmf">MetafileHeader::IsWmf</a> method determines whether the associated metafile is in the WMF format.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-iswmfplaceable">MetafileHeader::IsWmfPlaceable</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplusmetaheader/nf-gdiplusmetaheader-metafileheader-iswmfplaceable">MetafileHeader::IsWmfPlaceable</a> method determines whether the associated metafile is a placeable metafile.

</td>
</tr>
</table>

## -remarks

Metafiles provide a device-independent and application-independent way to share pictures. They contain records that describe a sequence of graphics APIs to invoke in a particular order with their associated graphics data. Metafiles can be recorded by an application and later played back by that application or by another one to reproduce a particular picture. They can also be used to send content to a print spooler. Enhanced metafiles support the ability to provide both Windows GDI+ and Windows Graphics Device Interface (GDI) descriptions of the same picture so that both GDI+ and down-level GDI applications can render it.
