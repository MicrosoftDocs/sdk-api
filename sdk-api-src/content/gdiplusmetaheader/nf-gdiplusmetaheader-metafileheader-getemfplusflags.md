---
UID: NF:gdiplusmetaheader.MetafileHeader.GetEmfPlusFlags
title: MetafileHeader::GetEmfPlusFlags (gdiplusmetaheader.h)
author: windows-sdk-content
description: The MetafileHeader::GetEmfPlusFlags method gets a flag that indicates whether the associated metafile was recorded against a video display device context.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetEmfPlusFlags_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getemfplusflags.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEmfPlusFlags, GetEmfPlusFlags method [GDI+], GetEmfPlusFlags method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetEmfPlusFlags method, MetafileHeader.GetEmfPlusFlags, MetafileHeader::GetEmfPlusFlags, _gdiplus_CLASS_MetafileHeader_GetEmfPlusFlags_, gdiplus._gdiplus_CLASS_MetafileHeader_GetEmfPlusFlags_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - MetafileHeader.GetEmfPlusFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# MetafileHeader::GetEmfPlusFlags


## -description


The <b>MetafileHeader::GetEmfPlusFlags</b> method gets a flag that indicates whether the associated metafile was recorded against a video display device context.


## -parameters






## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

If the associated metafile is in the EMF+ format and was recorded against a video display device context, then this method returns GDIP_EMFPLUSFLAGS_DISPLAY; otherwise, it returns 0. GDIP_EMFPLUSFLAGS_DISPLAY is defined in Gdiplusmetaheader.h.




## -see-also




<a href="https://docs.microsoft.com/previous-versions//ms535280(v=vs.85)">GetMetafileHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-metafiles-about">Metafiles</a>
 

 

