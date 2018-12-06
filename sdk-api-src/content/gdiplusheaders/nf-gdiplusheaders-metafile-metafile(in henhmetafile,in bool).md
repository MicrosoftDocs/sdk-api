---
UID: NF:gdiplusheaders.Metafile.Metafile(IN HENHMETAFILE,IN BOOL)
title: Metafile::Metafile(IN HENHMETAFILE,IN BOOL)
author: windows-sdk-content
description: Creates a Windows GDI+ Metafile::Metafile object for playback based on a Windows Graphics Device Interface (GDI) Enhanced Metafile (EMF) file.
old-location: gdiplus\_gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafileconstructors\metafile_91hemf_deleteemf.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Metafile, Metafile class [GDI+],Metafile constructor, Metafile constructor [GDI+], Metafile constructor [GDI+],Metafile class, Metafile.Metafile, Metafile.Metafile(HENHMETAFILE,BOOL), Metafile.Metafile(IN HENHMETAFILE,IN BOOL), Metafile::Metafile, Metafile::Metafile(IN HENHMETAFILE,IN BOOL), _gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_, gdiplus._gdiplus_CLASS_Metafile_Metafile_hEmf_deleteEmf_
ms.prod: windows-hardware
ms.technology: windows-devices
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

# Metafile::Metafile(IN HENHMETAFILE,IN BOOL)


## -description


Creates a Windows GDI+ <b>Metafile::Metafile</b> object for playback based on a Windows Graphics Device Interface (GDI) Enhanced Metafile (EMF) file.


## -parameters




### -param hEmf [in]

Type: <b>HENHMETAFILE</b>

Windows handle to a metafile. 


### -param deleteEmf [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the Windows handle to a metafile is deleted when the <b>Metafile::Metafile</b> object is deleted. <b>TRUE</b> specifies that the <i>hEmf</i> Windows handle is deleted, and <b>FALSE</b> specifies that the <i>hEmf</i> Windows handle is not deleted. The default value is <b>FALSE</b>. 


## -remarks



This constructor allows GDI+ to own the windows handle to the metafile, which should not be used by other portions of your code until the <b>Metafile::Metafile</b> object is deleted or goes out of scope.




## -see-also




<a href="https://msdn.microsoft.com/79b8df1b-6fc5-455b-9d08-57d64bf6bffa">Loading and Displaying Metafiles</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/538d8376-8922-41ba-abbc-0242474ec4fb">Metafile::GetHENHMETAFILE</a>



<a href="https://msdn.microsoft.com/a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077">Metafiles</a>



<a href="https://msdn.microsoft.com/062de6c2-9f82-415d-860e-2d1afd2ac027">Recording Metafiles</a>
 

 

