---
UID: NF:gdiplusheaders.Metafile.Metafile(IN const WCHAR,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)
title: Metafile::Metafile(IN const WCHAR,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)
author: windows-sdk-content
description: This topic lists the constructors of the Metafile class. For a complete class listing, see Metafile Class.
old-location: gdiplus\_gdiplus_CLASS_Metafile_Constructors.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Metafile, Metafile constructors [GDI+], Metafile.Metafile, Metafile.Metafile(IN const WCHAR,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), Metafile::Metafile, Metafile::Metafile(IN const WCHAR,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), _gdiplus_CLASS_Metafile_Constructors, gdiplus._gdiplus_CLASS_Metafile_Constructors, gdiplusheaders/Metafile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# Metafile::Metafile(IN const WCHAR,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)


## -description


<span>This topic lists the constructors of the 
		<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> class. For a complete class listing, see <b>Metafile Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bccba1d-63e4-469d-a7b8-0f83ff7ebcc0">Metafile(WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/1bccba1d-63e4-469d-a7b8-0f83ff7ebcc0">Metafile::Metafile</a> object for playback.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28d4fe40-b021-4b04-a6cb-55230aec4075">Metafile(IStream*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/28d4fe40-b021-4b04-a6cb-55230aec4075">Metafile::Metafile</a> object from an <a href="_stg_istream">IStream</a> interface for playback.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/843c1644-cf2e-4c46-afc3-17b51a2e9f70">Metafile(HENHMETAFILE,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a GDI+ <a href="https://msdn.microsoft.com/843c1644-cf2e-4c46-afc3-17b51a2e9f70">Metafile::Metafile</a> object for playback based on a GDI Enhanced Metafile (EMF) file.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6ea4143-4267-43a4-b0eb-86e063bc545b">Metafile(HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/b6ea4143-4267-43a4-b0eb-86e063bc545b">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7caf5e09-490c-4389-81a9-d495e56f8615">Metafile(WCHAR*,HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/7caf5e09-490c-4389-81a9-d495e56f8615">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82943279-26d5-4f42-af9b-c6007e5185ec">Metafile(IStream*,HDC,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/82943279-26d5-4f42-af9b-c6007e5185ec">Metafile::Metafile</a> object for recording to an <a href="_stg_istream">IStream</a> interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73a6eb0d-5c49-4570-8df8-0fe7d07cf8c7">Metafile(HMETAFILE,WmfPlaceableFileHeader*,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a GDI+<a href="https://msdn.microsoft.com/73a6eb0d-5c49-4570-8df8-0fe7d07cf8c7">Metafile::Metafile</a> object for recording. The format will be placeable metafile.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ede9f8a8-a0a3-4ed8-a673-26e6a1b95f58">Metafile(HDC,Rect&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/ede9f8a8-a0a3-4ed8-a673-26e6a1b95f58">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1a5ee44-f4c5-4cde-a980-e8a3bfe1cddb">Metafile(HDC,RectF&,MetaFileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/e1a5ee44-f4c5-4cde-a980-e8a3bfe1cddb">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5b62e57-17c3-47e1-ae91-dc196a6a458e">Metafile(WCHAR*,HDC,Rect&,MetaFileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/a5b62e57-17c3-47e1-ae91-dc196a6a458e">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a59ca3d-7b74-4fc6-a9ea-c741578df650">Metafile(WCHAR*,HDC,RectF&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/7a59ca3d-7b74-4fc6-a9ea-c741578df650">Metafile::Metafile</a> object for recording.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cef1deb-8f0e-460e-926d-f76a45a2016e">Metafile(IStream*,HDC,Rect&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/0cef1deb-8f0e-460e-926d-f76a45a2016e">Metafile::Metafile</a> object for recording to an <a href="_stg_istream">IStream</a> interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df4a2083-50f8-4ffa-9dbf-bfbeb2f35cb8">Metafile(IStream*,HDC,RectF&,MetafileFrameUnit,EmfType,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/df4a2083-50f8-4ffa-9dbf-bfbeb2f35cb8">Metafile::Metafile</a> object for recording to an <a href="_stg_istream">IStream</a> interface.

</td>
</tr>
</table>

## -parameters

