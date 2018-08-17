---
UID: NF:gdiplusmetaheader.MetafileHeader.GetWmfHeader
title: MetafileHeader::GetWmfHeader
author: windows-sdk-content
description: The MetafileHeader::GetWmfHeader method gets a METAHEADER structure that contains properties of the associated metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetWmfHeader_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getwmfheader.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetWmfHeader, GetWmfHeader method [GDI+], GetWmfHeader method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetWmfHeader method, MetafileHeader.GetWmfHeader, MetafileHeader::GetWmfHeader, _gdiplus_CLASS_MetafileHeader_GetWmfHeader_, gdiplus._gdiplus_CLASS_MetafileHeader_GetWmfHeader_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusmetaheader.h
req.include-header: Gdiplus.h
req.redist: 
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
 - MetafileHeader.GetWmfHeader
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# MetafileHeader::GetWmfHeader


## -description


The <b>MetafileHeader::GetWmfHeader</b> method gets a <a href="https://msdn.microsoft.com/3ad5be24-9558-442e-8c77-dd6a7d33c208">METAHEADER</a> structure that contains properties of the associated metafile.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/3ad5be24-9558-442e-8c77-dd6a7d33c208">METAHEADER</a>*</b>
</strong>

If the associated metafile is in the WMF format, this method returns a pointer to a structure that contains properties of the associated metafile. If the associated metafile is in the EMF or EMF+ format, this method returns <b>NULL</b>. The <a href="https://msdn.microsoft.com/3ad5be24-9558-442e-8c77-dd6a7d33c208">METAHEADER</a> structure is defined in Wingdi.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535280(v=VS.85).aspx">GetMetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/3ad5be24-9558-442e-8c77-dd6a7d33c208">METAHEADER</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

