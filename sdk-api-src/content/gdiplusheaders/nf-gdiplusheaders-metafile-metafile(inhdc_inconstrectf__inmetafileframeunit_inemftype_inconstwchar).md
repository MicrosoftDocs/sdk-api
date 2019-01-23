---
UID: NF:gdiplusheaders.Metafile.Metafile(IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)
title: Metafile::Metafile(IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)
author: windows-sdk-content
description: Creates a Metafile::Metafile object for recording.
old-location: gdiplus\_gdiplus_CLASS_Metafile_Metafile_HDC_referenceHdc_RectF_frameRect_MetafileFrameUnit_frameUnit_EmfTyp.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors\metafile_30hdcreferencehdc_rectfampframerect_meta.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Metafile, Metafile class [GDI+],Metafile constructor, Metafile constructor [GDI+], Metafile constructor [GDI+],Metafile class, Metafile.Metafile, Metafile.Metafile(HDC,const RectF&,MetaFileFrameUnit,EmfType,const WCHAR*), Metafile.Metafile(IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), Metafile::Metafile, Metafile::Metafile(IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR), _gdiplus_CLASS_Metafile_Metafile_HDC_referenceHdc_RectF_frameRect_MetafileFrameUnit_frameUnit_EmfTyp, gdiplus._gdiplus_CLASS_Metafile_Metafile_HDC_referenceHdc_RectF_frameRect_MetafileFrameUnit_frameUnit_EmfTyp
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

# Metafile::Metafile(IN HDC,IN const RectF &,IN MetafileFrameUnit,IN EmfType,IN const WCHAR)


## -description


Creates a <b>Metafile::Metafile</b> object for recording.


## -parameters




### -param referenceHdc [in]

Type: <b>HDC</b>

Windows handle to a device context that contains attributes of the display device that is used to record the metafile. 


### -param frameRect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a></b>

Reference to a rectangle that bounds the metafile display. 


### -param frameUnit [in]

Type: <b>MetaFileFrameUnit</b>

Optional. Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534151(v=VS.85).aspx">MetafileFrameUnit</a> enumeration that specifies the unit of measure for <i>frameRect</i>. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534151(v=VS.85).aspx">MetafileFrameUnitGdi</a>. 


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
 

 

