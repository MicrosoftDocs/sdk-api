---
UID: NE:docobj.__MIDL_IOleDocument_0001
title: DOCMISC (docobj.h)
description: Provides miscellaneous property information about a document object.
helpviewer_keywords: ["DOCMISC","DOCMISC enumeration [COM]","DOCMISC_CANCREATEMULTIPLEVIEWS","DOCMISC_CANTOPENEDIT","DOCMISC_NOFILESUPPORT","DOCMISC_SUPPORTCOMPLEXRECTANGLES","_ole_DOCMISC","com.docmisc","docobj/DOCMISC","docobj/DOCMISC_CANCREATEMULTIPLEVIEWS","docobj/DOCMISC_CANTOPENEDIT","docobj/DOCMISC_NOFILESUPPORT","docobj/DOCMISC_SUPPORTCOMPLEXRECTANGLES"]
old-location: com\docmisc.htm
tech.root: com
ms.assetid: e52e022e-dd82-42f0-a3dd-2730ad80613c
ms.date: 12/05/2018
ms.keywords: DOCMISC, DOCMISC enumeration [COM], DOCMISC_CANCREATEMULTIPLEVIEWS, DOCMISC_CANTOPENEDIT, DOCMISC_NOFILESUPPORT, DOCMISC_SUPPORTCOMPLEXRECTANGLES, _ole_DOCMISC, com.docmisc, docobj/DOCMISC, docobj/DOCMISC_CANCREATEMULTIPLEVIEWS, docobj/DOCMISC_CANTOPENEDIT, docobj/DOCMISC_NOFILESUPPORT, docobj/DOCMISC_SUPPORTCOMPLEXRECTANGLES
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
targetos: Windows
req.typenames: DOCMISC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL_IOleDocument_0001
 - docobj/__MIDL_IOleDocument_0001
 - DOCMISC
 - docobj/DOCMISC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DocObj.h
api_name:
 - DOCMISC
---

# DOCMISC enumeration


## -description

Provides miscellaneous property information about a document object.

## -enum-fields

### -field DOCMISC_CANCREATEMULTIPLEVIEWS:1

Object supports multiple views.

### -field DOCMISC_SUPPORTCOMPLEXRECTANGLES:2

Object supports complex rectangles and therefore implements <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">IOleDocumentView::SetRectComplex</a>.

### -field DOCMISC_CANTOPENEDIT:4

Object supports activation in a separate window and therefore implements <a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-open">IOleDocumentView::Open</a>.

### -field DOCMISC_NOFILESUPPORT:8

Object does not support file read/write.

## -remarks

Objects that have a limited user interface for activation purposes should set DOCMISC_CANTOPENEDIT. Those that support <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a> only as a persistence mechanism should specify DOCMISC_NOFILESUPPORT. Otherwise, an object must also implement <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>.

A combination of values from <b>DOCMISC</b> is returned at the location specified by the <i>pdwStatus</i> parameter in <a href="/windows/desktop/api/docobj/nf-docobj-ioledocument-getdocmiscstatus">IOleDocument::GetDocMiscStatus</a>.

If an object requires none of these flags, it must write a zero to the <i>pdwStatus</i> parameter.

## -see-also

<a href="/windows/desktop/api/docobj/nf-docobj-ioledocument-getdocmiscstatus">IOleDocument::GetDocMiscStatus</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-open">IOleDocumentView::Open</a>



<a href="/windows/desktop/api/docobj/nf-docobj-ioledocumentview-setrectcomplex">IOleDocumentView::SetRectComplex</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>
