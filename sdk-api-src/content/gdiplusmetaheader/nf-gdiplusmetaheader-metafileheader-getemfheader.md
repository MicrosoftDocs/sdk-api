---
UID: NF:gdiplusmetaheader.MetafileHeader.GetEmfHeader
title: MetafileHeader::GetEmfHeader
author: windows-sdk-content
description: The MetafileHeader::GetEmfHeader method gets an ENHMETAHEADER3 structure that contains properties of the associated metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetEmfHeader_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getemfheader.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetEmfHeader, GetEmfHeader method [GDI+], GetEmfHeader method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetEmfHeader method, MetafileHeader.GetEmfHeader, MetafileHeader::GetEmfHeader, _gdiplus_CLASS_MetafileHeader_GetEmfHeader_, gdiplus._gdiplus_CLASS_MetafileHeader_GetEmfHeader_
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# MetafileHeader::GetEmfHeader


## -description


The <b>MetafileHeader::GetEmfHeader</b> method gets an <a href="https://msdn.microsoft.com/48cacd83-8123-476c-af78-11ad41285c3e">ENHMETAHEADER3</a> structure that contains properties of the associated metafile.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/48cacd83-8123-476c-af78-11ad41285c3e">ENHMETAHEADER3</a>*</b>
</strong>

If the associated metafile is in the EMF or EMF+ format, this method returns a pointer to an <a href="https://msdn.microsoft.com/48cacd83-8123-476c-af78-11ad41285c3e">ENHMETAHEADER3</a> structure that contains properties of the associated metafile. If the associated metafile is in the WMF format, this method returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/48cacd83-8123-476c-af78-11ad41285c3e">ENHMETAHEADER3</a>



<a href="https://msdn.microsoft.com/e7f1f35d-f229-4053-b508-19ad00068195">GetMetafileHeader</a>



<a href="https://msdn.microsoft.com/79b8df1b-6fc5-455b-9d08-57d64bf6bffa">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/4ea75699-c3c7-481e-b369-3bdc600b9713">MetafileHeader</a>



<a href="https://msdn.microsoft.com/a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077">Metafiles</a>
 

 

