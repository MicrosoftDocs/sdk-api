---
UID: NF:gdiplusheaders.Metafile.Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)
title: Metafile::Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)
author: windows-sdk-content
description: This topic lists the constructors of the Metafile class. For a complete class listing, see Metafile Class.
old-location: gdiplus\_gdiplus_CLASS_Metafile_Constructors.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Metafile, Metafile constructors [GDI+], Metafile.Metafile, Metafile.Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), Metafile::Metafile, Metafile::Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), _gdiplus_CLASS_Metafile_Constructors, gdiplus._gdiplus_CLASS_Metafile_Constructors, gdiplusheaders/Metafile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gdiplusheaders.h
api_name:
 - Metafile.Metafile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# Metafile::Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)


## -description


<span>This topic lists the constructors of the 
		<a href="https://msdn.microsoft.com/library/ms534477(v=VS.85).aspx">Metafile</a> class. For a complete class listing, see <b>Metafile Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535285(v=VS.85).aspx">Metafile(WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535285(v=VS.85).aspx">Metafile::Metafile</a> object for playback.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535294(v=VS.85).aspx">Metafile(IStream*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535294(v=VS.85).aspx">Metafile::Metafile</a> object from an <a href="https://msdn.microsoft.com/library/Aa380034(v=VS.85).aspx">IStream</a> interface for playback.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535295(v=VS.85).aspx">Metafile(HENHMETAFILE,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a GDI+ <a href="https://msdn.microsoft.com/library/ms535295(v=VS.85).aspx">Metafile::Metafile</a> object for playback based on a GDI Enhanced Metafile (EMF) file.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535284(v=VS.85).aspx">Metafile(HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535284(v=VS.85).aspx">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535293(v=VS.85).aspx">Metafile(WCHAR*,HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535293(v=VS.85).aspx">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535290(v=VS.85).aspx">Metafile(IStream*,HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535290(v=VS.85).aspx">Metafile::Metafile</a> object for recording to an <a href="https://msdn.microsoft.com/library/Aa380034(v=VS.85).aspx">IStream</a> interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535287(v=VS.85).aspx">Metafile(HMETAFILE,WmfPlaceableFileHeader*,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a GDI+<a href="https://msdn.microsoft.com/library/ms535287(v=VS.85).aspx">Metafile::Metafile</a> object for recording. The format will be placeable metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535296(v=VS.85).aspx">Metafile(HDC,Rect&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535296(v=VS.85).aspx">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535286(v=VS.85).aspx">Metafile(HDC,RectF&,MetaFileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535286(v=VS.85).aspx">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535288(v=VS.85).aspx">Metafile(WCHAR*,HDC,Rect&,MetaFileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535288(v=VS.85).aspx">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535292(v=VS.85).aspx">Metafile(WCHAR*,HDC,RectF&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535292(v=VS.85).aspx">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535291(v=VS.85).aspx">Metafile(IStream*,HDC,Rect&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535291(v=VS.85).aspx">Metafile::Metafile</a> object for recording to an <a href="https://msdn.microsoft.com/library/Aa380034(v=VS.85).aspx">IStream</a> interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms535289(v=VS.85).aspx">Metafile(IStream*,HDC,RectF&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535289(v=VS.85).aspx">Metafile::Metafile</a> object for recording to an <a href="https://msdn.microsoft.com/library/Aa380034(v=VS.85).aspx">IStream</a> interface.

</td>
</tr>
</table>

## -parameters

