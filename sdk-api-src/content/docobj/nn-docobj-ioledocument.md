---
UID: NN:docobj.IOleDocument
title: IOleDocument (docobj.h)
description: Enables a document object to communicate to containers its ability to create views of its data.
old-location: com\ioledocument.htm
tech.root: com
ms.assetid: 7a15d6ef-900c-4a0b-8b85-60dc66ca03a3
ms.date: 12/05/2018
ms.keywords: IOleDocument, IOleDocument interface [COM], IOleDocument interface [COM],described, _ole_ioledocument, com.ioledocument, docobj/IOleDocument
ms.topic: interface
f1_keywords:
- docobj/IOleDocument
dev_langs:
- c++
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.Idl
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
- COM
api_location:
- DocObj.h
api_name:
- IOleDocument
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleDocument interface


## -description


Enables a document object to communicate to containers its ability to create views of its data. This interface also enables a document object to enumerate its views and to provide containers with miscellaneous information about itself, such as whether it supports multiple views or complex rectangles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleDocument</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocument-createview">CreateView</a>
</td>
<td align="left" width="63%">
Creates a document view object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocument-enumviews">EnumViews</a>
</td>
<td align="left" width="63%">
Creates an object that enumerates the views supported by a document object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-ioledocument-getdocmiscstatus">GetDocMiscStatus</a>
</td>
<td align="left" width="63%">
Retrieves status information about the document object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-iolecommandtarget">IOleCommandTarget</a>



<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-ioledocumentsite">IOleDocumentSite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-ioledocumentview">IOleDocumentView</a>



<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a>
 

 

