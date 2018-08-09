---
UID: NF:gdiplusmetaheader.MetafileHeader.GetEmfPlusFlags
title: MetafileHeader::GetEmfPlusFlags
author: windows-sdk-content
description: The MetafileHeader::GetEmfPlusFlags method gets a flag that indicates whether the associated metafile was recorded against a video display device context.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetEmfPlusFlags_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getemfplusflags.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEmfPlusFlags, GetEmfPlusFlags method [GDI+], GetEmfPlusFlags method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetEmfPlusFlags method, MetafileHeader.GetEmfPlusFlags, MetafileHeader::GetEmfPlusFlags, _gdiplus_CLASS_MetafileHeader_GetEmfPlusFlags_, gdiplus._gdiplus_CLASS_MetafileHeader_GetEmfPlusFlags_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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




<a href="https://msdn.microsoft.com/en-us/library/ms535280(v=VS.85).aspx">GetMetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

