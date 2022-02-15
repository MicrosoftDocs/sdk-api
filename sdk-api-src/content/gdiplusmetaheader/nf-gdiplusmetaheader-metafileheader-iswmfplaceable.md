---
UID: NF:gdiplusmetaheader.MetafileHeader.IsWmfPlaceable
title: MetafileHeader::IsWmfPlaceable (gdiplusmetaheader.h)
description: The MetafileHeader::IsWmfPlaceable method determines whether the associated metafile is a placeable metafile.
helpviewer_keywords: ["IsWmfPlaceable","IsWmfPlaceable method [GDI+]","IsWmfPlaceable method [GDI+]","MetafileHeader class","MetafileHeader class [GDI+]","IsWmfPlaceable method","MetafileHeader.IsWmfPlaceable","MetafileHeader::IsWmfPlaceable","_gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_","gdiplus._gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_"]
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\iswmfplaceable.htm
ms.date: 12/05/2018
ms.keywords: IsWmfPlaceable, IsWmfPlaceable method [GDI+], IsWmfPlaceable method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],IsWmfPlaceable method, MetafileHeader.IsWmfPlaceable, MetafileHeader::IsWmfPlaceable, _gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_, gdiplus._gdiplus_CLASS_MetafileHeader_IsWmfPlaceable_
req.header: gdiplusmetaheader.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - MetafileHeader::IsWmfPlaceable
 - gdiplusmetaheader/MetafileHeader::IsWmfPlaceable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - MetafileHeader.IsWmfPlaceable
---

# MetafileHeader::IsWmfPlaceable


## -description

The <b>MetafileHeader::IsWmfPlaceable</b> method determines whether the associated metafile is a placeable metafile.



## -returns

Type: <b>BOOL</b>

If the associated metafile is a placeable metafile, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -remarks

Placeable metafiles are .wmf files that contain a preheader preceding the metafile header. The preheader contains additional information for the metafile header of the metafile.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a> object from a .wmf file and gets the metafile header of the metafile. The code then determines whether the metafile is a placeable metafile.


```cpp

MetafileHeader metaHeader;
Metafile::GetMetafileHeader(L"sampleMetafile.wmf", &metaHeader);

if(metaHeader.IsWmfPlaceable() == TRUE)
{
   // The associated metafile is a placeable metafile.
}
				
```

## -see-also

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
