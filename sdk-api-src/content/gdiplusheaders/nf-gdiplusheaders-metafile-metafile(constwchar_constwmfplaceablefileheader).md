---
UID: NF:gdiplusheaders.Metafile.Metafile(constWCHAR,constWmfPlaceableFileHeader)
title: Metafile::Metafile(IN const WCHAR,IN const WmfPlaceableFileHeader) (gdiplusheaders.h)
description: This topic lists the constructors of the Metafile class. For a complete class listing, see Metafile Class. (overload 1/2)
helpviewer_keywords: ["Metafile","Metafile constructors [GDI+]","Metafile.Metafile","Metafile.Metafile(IN const WCHAR","IN const WmfPlaceableFileHeader)","Metafile::Metafile","Metafile::Metafile(IN const WCHAR","IN const WmfPlaceableFileHeader)","_gdiplus_CLASS_Metafile_Constructors","gdiplus._gdiplus_CLASS_Metafile_Constructors","gdiplusheaders/Metafile"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_Constructors.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors.htm
ms.date: 12/05/2018
ms.keywords: Metafile, Metafile constructors [GDI+], Metafile.Metafile, Metafile.Metafile(IN const WCHAR,IN const WmfPlaceableFileHeader), Metafile::Metafile, Metafile::Metafile(IN const WCHAR,IN const WmfPlaceableFileHeader), _gdiplus_CLASS_Metafile_Constructors, gdiplus._gdiplus_CLASS_Metafile_Constructors, gdiplusheaders/Metafile
req.header: gdiplusheaders.h
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
 - Metafile::Metafile
 - gdiplusheaders/Metafile::Metafile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gdiplusheaders.h
api_name:
 - Metafile.Metafile
---

# Metafile::Metafile(IN const WCHAR,IN const WmfPlaceableFileHeader)


## -description

<span>This topic lists the constructors of the 
		<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a> class. For a complete class listing, see <b>Metafile Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535285(v=vs.85)">Metafile(WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535285(v=vs.85)">Metafile::Metafile</a> object for playback.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535294(v=vs.85)">Metafile(IStream*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535294(v=vs.85)">Metafile::Metafile</a> object from an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface for playback.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool)">Metafile(HENHMETAFILE,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a GDI+ <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(inhenhmetafile_inbool)">Metafile::Metafile</a> object for playback based on a GDI Enhanced Metafile (EMF) file.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535284(v=vs.85)">Metafile(HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535284(v=vs.85)">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535293(v=vs.85)">Metafile(WCHAR*,HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535293(v=vs.85)">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535290(v=vs.85)">Metafile(IStream*,HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535290(v=vs.85)">Metafile::Metafile</a> object for recording to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535287(v=vs.85)">Metafile(HMETAFILE,WmfPlaceableFileHeader*,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a GDI+<a href="/previous-versions/ms535287(v=vs.85)">Metafile::Metafile</a> object for recording. The format will be placeable metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535296(v=vs.85)">Metafile(HDC,Rect&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535296(v=vs.85)">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535286(v=vs.85)">Metafile(HDC,RectF&,MetaFileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535286(v=vs.85)">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535288(v=vs.85)">Metafile(WCHAR*,HDC,Rect&,MetaFileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535288(v=vs.85)">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535292(v=vs.85)">Metafile(WCHAR*,HDC,RectF&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535292(v=vs.85)">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535291(v=vs.85)">Metafile(IStream*,HDC,Rect&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535291(v=vs.85)">Metafile::Metafile</a> object for recording to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/previous-versions/ms535289(v=vs.85)">Metafile(IStream*,HDC,RectF&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/previous-versions/ms535289(v=vs.85)">Metafile::Metafile</a> object for recording to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface.

</td>
</tr>
</table>

## -parameters
