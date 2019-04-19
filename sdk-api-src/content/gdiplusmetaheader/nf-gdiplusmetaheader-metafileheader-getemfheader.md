---
UID: NF:gdiplusmetaheader.MetafileHeader.GetEmfHeader
title: MetafileHeader::GetEmfHeader (gdiplusmetaheader.h)
author: windows-sdk-content
description: The MetafileHeader::GetEmfHeader method gets an ENHMETAHEADER3 structure that contains properties of the associated metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetEmfHeader_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getemfheader.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEmfHeader, GetEmfHeader method [GDI+], GetEmfHeader method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetEmfHeader method, MetafileHeader.GetEmfHeader, MetafileHeader::GetEmfHeader, _gdiplus_CLASS_MetafileHeader_GetEmfHeader_, gdiplus._gdiplus_CLASS_MetafileHeader_GetEmfHeader_
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
 - MetafileHeader.GetEmfHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# MetafileHeader::GetEmfHeader


## -description


The <b>MetafileHeader::GetEmfHeader</b> method gets an <a href="https://msdn.microsoft.com/en-us/library/ms534065(v=VS.85).aspx">ENHMETAHEADER3</a> structure that contains properties of the associated metafile.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534065(v=VS.85).aspx">ENHMETAHEADER3</a>*</b>
</strong>

If the associated metafile is in the EMF or EMF+ format, this method returns a pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534065(v=VS.85).aspx">ENHMETAHEADER3</a> structure that contains properties of the associated metafile. If the associated metafile is in the WMF format, this method returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534065(v=VS.85).aspx">ENHMETAHEADER3</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535280(v=VS.85).aspx">GetMetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

