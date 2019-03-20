---
UID: NF:gdiplusheaders.Metafile.Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)
title: Metafile::Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR) (gdiplusheaders.h)
author: windows-sdk-content
description: Creates a Metafile::Metafile object for recording to an IStream interface.
old-location: gdiplus\_gdiplus_CLASS_Metafile_Metafile_IStream_stream_HDC_referenceHdc_RectF_frameRect_MetafileFrameUnit_f.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors\metafile_48istreamstream_hdcreferencehdc_rectfamp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Metafile, Metafile class [GDI+],Metafile constructor, Metafile constructor [GDI+], Metafile constructor [GDI+],Metafile class, Metafile.Metafile, Metafile.Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), Metafile.Metafile(IStream*,HDC,const RectF&,MetafileFrameUnit,EmfType,const WCHAR*), Metafile::Metafile, Metafile::Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), _gdiplus_CLASS_Metafile_Metafile_IStream_stream_HDC_referenceHdc_RectF_frameRect_MetafileFrameUnit_f, gdiplus._gdiplus_CLASS_Metafile_Metafile_IStream_stream_HDC_referenceHdc_RectF_frameRect_MetafileFrameUnit_f
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
 - Metafile.Metafile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Metafile::Metafile(IN IStream,IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)


## -description


Creates a <b>Metafile::Metafile</b> object for recording to an <a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a> interface.


## -parameters




### -param stream [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a>*</b>

Pointer to a COM <a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a> interface that points to a stream of data in a file. When the commands are recorded, they will be saved to this stream. 


### -param referenceHdc [in]

Type: <b>HDC</b>

Windows handle to a device context that contains attributes of the display device that is used to record the metafile. 


### -param frameRect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a></b>

Reference to a rectangle that bounds the metafile display. 


### -param frameUnit [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534151(v=VS.85).aspx">MetafileFrameUnit</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534151(v=VS.85).aspx">MetafileFrameUnit</a> enumeration that specifies the unit of measure for 
					<i>frameRect</i>. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534151(v=VS.85).aspx">MetafileFrameUnitGdi</a>. 


### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534115(v=VS.85).aspx">EmfType</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534115(v=VS.85).aspx">EmfType</a> enumeration that specifies the type of metafile that will be recorded. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534151(v=VS.85).aspx">EmfTypeEmfPlusDual</a>. 


### -param description [in]

Type: <b>const WCHAR*</b>

Optional. Pointer to a wide-character string that specifies the descriptive name of the metafile. The default value is <b>NULL</b>. 


## -remarks



When recording to a file, the file must be writable, and Windows GDI+ must be able to obtain an exclusive lock on the file.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534115(v=VS.85).aspx">EmfType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533831(v=VS.85).aspx">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534151(v=VS.85).aspx">MetafileFrameUnit</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536391(v=VS.85).aspx">Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533833(v=VS.85).aspx">Recording Metafiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>
 

 

