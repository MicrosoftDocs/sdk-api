---
UID: NF:gdiplusheaders.Metafile.GetMetafileHeader(IN IStream,OUT MetafileHeader)
title: Metafile::GetMetafileHeader(IN IStream,OUT MetafileHeader) (gdiplusheaders.h)
author: windows-sdk-content
description: The Metafile::GetMetafileHeader method gets the header.
old-location: gdiplus\_gdiplus_CLASS_Metafile_GetMetafileHeader_stream_header_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\metafilegetmetafileheadermethods\getmetafileheader_98stream_header.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMetafileHeader, GetMetafileHeader method [GDI+], GetMetafileHeader method [GDI+],Metafile class, Metafile class [GDI+],GetMetafileHeader method, Metafile.GetMetafileHeader, Metafile.GetMetafileHeader(IN IStream,OUT MetafileHeader), Metafile.GetMetafileHeader(IStream*,MetafileHeader*), Metafile::GetMetafileHeader, Metafile::GetMetafileHeader(IN IStream,OUT MetafileHeader), _gdiplus_CLASS_Metafile_GetMetafileHeader_stream_header_, gdiplus._gdiplus_CLASS_Metafile_GetMetafileHeader_stream_header_
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Metafile.GetMetafileHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Metafile::GetMetafileHeader(IN IStream,OUT MetafileHeader)


## -description


The <b>Metafile::GetMetafileHeader</b> method gets the header.


## -parameters




### -param stream [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a>*</b>

Pointer to a COM 
					<a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a> interface that points to a stream of data in a file. 


### -param header [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a> object that receives the header, which contains the attributes of the metafile. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns OK, which is an element of the 

						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534480(v=VS.85).aspx">MetafileHeader</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>
 

 

