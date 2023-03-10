---
UID: NF:gdiplusheaders.Metafile.GetHENHMETAFILE
title: Metafile::GetHENHMETAFILE (gdiplusheaders.h)
description: The Metafile::GetHENHMETAFILE method gets a Windows handle to an Enhanced Metafile (EMF) file.
helpviewer_keywords: ["GetHENHMETAFILE","GetHENHMETAFILE method [GDI+]","GetHENHMETAFILE method [GDI+]","Metafile class","Metafile class [GDI+]","GetHENHMETAFILE method","Metafile.GetHENHMETAFILE","Metafile::GetHENHMETAFILE","_gdiplus_CLASS_Metafile_GetHENHMETAFILE_","gdiplus._gdiplus_CLASS_Metafile_GetHENHMETAFILE_"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_GetHENHMETAFILE_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\gethenhmetafile.htm
ms.date: 12/05/2018
ms.keywords: GetHENHMETAFILE, GetHENHMETAFILE method [GDI+], GetHENHMETAFILE method [GDI+],Metafile class, Metafile class [GDI+],GetHENHMETAFILE method, Metafile.GetHENHMETAFILE, Metafile::GetHENHMETAFILE, _gdiplus_CLASS_Metafile_GetHENHMETAFILE_, gdiplus._gdiplus_CLASS_Metafile_GetHENHMETAFILE_
req.header: gdiplusheaders.h
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
 - Metafile::GetHENHMETAFILE
 - gdiplusheaders/Metafile::GetHENHMETAFILE
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
 - Metafile.GetHENHMETAFILE
---

# Metafile::GetHENHMETAFILE


## -description

The <b>Metafile::GetHENHMETAFILE</b> method gets a Windows handle to an Enhanced Metafile (EMF) file.



## -returns

Type: <b>HENHMETAFILE</b>

This method returns a <b>HENHMETAFILE</b>.

## -remarks

This method sets the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a> object to an invalid state. The user is responsible for calling DeleteEnhMetafile, to delete the Windows handle.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a> object from an EMF+ file and gets a Windows handle to the metafile.


```cpp
VOID Example_GetHENHMETAFILE(HDC hdc)
{

   // Create a GDI+ Metafile object from an existing disk file.
   Metafile metafile(L"SampleMetafile.emf+");

   // Get a Windows handle to the metafile.
   HENHMETAFILE hEmf = metafile.GetHENHMETAFILE();

}
```

## -see-also

<a href="/windows/desktop/api/gdiplusmetaheader/ns-gdiplusmetaheader-enhmetaheader3">ENHMETAHEADER3</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>
