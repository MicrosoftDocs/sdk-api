---
UID: NE:docobj.__MIDL_IOleDocument_0001
title: DOCMISC (docobj.h)
author: windows-sdk-content
description: Provides miscellaneous property information about a document object.
old-location: com\docmisc.htm
tech.root: com
ms.assetid: e52e022e-dd82-42f0-a3dd-2730ad80613c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DOCMISC, DOCMISC enumeration [COM], DOCMISC_CANCREATEMULTIPLEVIEWS, DOCMISC_CANTOPENEDIT, DOCMISC_NOFILESUPPORT, DOCMISC_SUPPORTCOMPLEXRECTANGLES, _ole_DOCMISC, com.docmisc, docobj/DOCMISC, docobj/DOCMISC_CANCREATEMULTIPLEVIEWS, docobj/DOCMISC_CANTOPENEDIT, docobj/DOCMISC_NOFILESUPPORT, docobj/DOCMISC_SUPPORTCOMPLEXRECTANGLES
ms.topic: enum
f1_keywords: 
 - "docobj/DOCMISC"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: DOCMISC
req.redist: 
ms.custom: 19H1
---

# DOCMISC enumeration


## -description


Provides miscellaneous property information about a document object. 


## -enum-fields




### -field DOCMISC_CANCREATEMULTIPLEVIEWS

Object supports multiple views.


### -field DOCMISC_SUPPORTCOMPLEXRECTANGLES

Object supports complex rectangles and therefore implements <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">IOleDocumentView::SetRectComplex</a>.


### -field DOCMISC_CANTOPENEDIT

Object supports activation in a separate window and therefore implements <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-open">IOleDocumentView::Open</a>.


### -field DOCMISC_NOFILESUPPORT

Object does not support file read/write.


## -remarks



Objects that have a limited user interface for activation purposes should set DOCMISC_CANTOPENEDIT. Those that support <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> only as a persistence mechanism should specify DOCMISC_NOFILESUPPORT. Otherwise, an object must also implement <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>.

A combination of values from <b>DOCMISC</b> is returned at the location specified by the <i>pdwStatus</i> parameter in <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocument-getdocmiscstatus">IOleDocument::GetDocMiscStatus</a>.

If an object requires none of these flags, it must write a zero to the <i>pdwStatus</i> parameter.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocument-getdocmiscstatus">IOleDocument::GetDocMiscStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-open">IOleDocumentView::Open</a>



<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">IOleDocumentView::SetRectComplex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>
 

 

