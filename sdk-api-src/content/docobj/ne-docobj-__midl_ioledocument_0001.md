---
UID: NE:docobj.__MIDL_IOleDocument_0001
title: "__MIDL_IOleDocument_0001"
author: windows-sdk-content
description: Provides miscellaneous property information about a document object.
old-location: com\docmisc.htm
old-project: com
ms.assetid: e52e022e-dd82-42f0-a3dd-2730ad80613c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DOCMISC, DOCMISC enumeration [COM], DOCMISC_CANCREATEMULTIPLEVIEWS, DOCMISC_CANTOPENEDIT, DOCMISC_NOFILESUPPORT, DOCMISC_SUPPORTCOMPLEXRECTANGLES, __MIDL_IOleDocument_0001, _ole_DOCMISC, com.docmisc, docobj/DOCMISC, docobj/DOCMISC_CANCREATEMULTIPLEVIEWS, docobj/DOCMISC_CANTOPENEDIT, docobj/DOCMISC_NOFILESUPPORT, docobj/DOCMISC_SUPPORTCOMPLEXRECTANGLES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: DOCMISC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DocObj.h
api_name:
 - DOCMISC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# __MIDL_IOleDocument_0001 enumeration


## -description


Provides miscellaneous property information about a document object. 


## -enum-fields




### -field DOCMISC_CANCREATEMULTIPLEVIEWS

Object supports multiple views.


### -field DOCMISC_SUPPORTCOMPLEXRECTANGLES

Object supports complex rectangles and therefore implements <a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>.


### -field DOCMISC_CANTOPENEDIT

Object supports activation in a separate window and therefore implements <a href="https://msdn.microsoft.com/46f801ae-ae03-4567-9442-cf3fbb6d06d7">IOleDocumentView::Open</a>.


### -field DOCMISC_NOFILESUPPORT

Object does not support file read/write.


## -remarks



Objects that have a limited user interface for activation purposes should set DOCMISC_CANTOPENEDIT. Those that support <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a> only as a persistence mechanism should specify DOCMISC_NOFILESUPPORT. Otherwise, an object must also implement <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>.

A combination of values from <b>DOCMISC</b> is returned at the location specified by the <i>pdwStatus</i> parameter in <a href="https://msdn.microsoft.com/de279d46-057e-4c3a-8af3-14f7b65147fd">IOleDocument::GetDocMiscStatus</a>.

If an object requires none of these flags, it must write a zero to the <i>pdwStatus</i> parameter.





## -see-also




<a href="https://msdn.microsoft.com/de279d46-057e-4c3a-8af3-14f7b65147fd">IOleDocument::GetDocMiscStatus</a>



<a href="https://msdn.microsoft.com/46f801ae-ae03-4567-9442-cf3fbb6d06d7">IOleDocumentView::Open</a>



<a href="https://msdn.microsoft.com/d220b200-85cb-43ff-a59d-147c14eef544">IOleDocumentView::SetRectComplex</a>



<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>



<a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>
 

 

