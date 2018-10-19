---
UID: NF:gdiplusmetaheader.MetafileHeader.GetVersion
title: MetafileHeader::GetVersion
author: windows-sdk-content
description: The MetafileHeader::GetVersion method gets the version of the metafile.
old-location: gdiplus\_gdiplus_CLASS_MetafileHeader_GetVersion_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileheaderclass\metafileheadermethods\getversion.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetVersion, GetVersion method [GDI+], GetVersion method [GDI+],MetafileHeader class, MetafileHeader class [GDI+],GetVersion method, MetafileHeader.GetVersion, MetafileHeader::GetVersion, _gdiplus_CLASS_MetafileHeader_GetVersion_, gdiplus._gdiplus_CLASS_MetafileHeader_GetVersion_
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
 - MetafileHeader.GetVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# MetafileHeader::GetVersion


## -description


The <b>MetafileHeader::GetVersion</b> method gets the version of the metafile.


## -parameters






## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns the version of the metafile. The metafile version indicates whether the metafile is an EMF, EMF+, or WMF metafile. EMF files always have 0x0010000 as the version. EMF+ files currently have 0xdbc01001 as the version. WMF files usually have 0x0300 as the version; however, earlier versions may be 0x0100.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535280(v=VS.85).aspx">GetMetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

