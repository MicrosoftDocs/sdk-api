---
UID: NN:textstor.ITextStoreAnchor
title: ITextStoreAnchor (textstor.h)
description: The ITextStoreAnchor interface is implemented by a Microsoft Active Accessibility client and is used by the TSF manager to manipulate text streams.
old-location: tsf\itextstoreanchor.htm
tech.root: TSF
ms.assetid: 62730a6d-4dc8-4207-9818-ab95e6537854
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor, ITextStoreAnchor interface [Text Services Framework], ITextStoreAnchor interface [Text Services Framework],described, _tsf_itextstoreanchor_ref, textstor/ITextStoreAnchor, tsf.itextstoreanchor
f1_keywords:
- textstor/ITextStoreAnchor
dev_langs:
- c++
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITextStoreAnchor
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreAnchor interface


## -description


The ITextStoreAnchor interface is implemented by a <a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a> client and is used by the TSF manager to manipulate text streams. <a href="https://docs.microsoft.com/windows/desktop/TSF/ranges">Ranges</a> of text within a stream are delimited by <a href="https://docs.microsoft.com/windows/desktop/TSF/ranges">anchor</a> objects. these anchor objects are exposed and manipulated by the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-ianchor">IAnchor</a> interface.

An application can obtain an instance of this interface with <a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>. The interface ID is IID_ITextStoreAnchor.

To use the application character position (ACP) model for text manipulation, use <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> instead.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreAnchor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreAnchor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoreAnchor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">AdviseSink</a>
</td>
<td align="left" width="63%">
Installs a new advise sink or modifies an existing advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-findnextattrtransition">FindNextAttrTransition</a>
</td>
<td align="left" width="63%">
Finds the location in the text stream where a transition occurs in an attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getactiveview">GetActiveView</a>
</td>
<td align="left" width="63%">
Returns a TsViewCookie data type that specifies the current active view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getanchorfrompoint">GetAnchorFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point in screen coordinates to an anchor positioned at a corresponding location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getembedded">GetEmbedded</a>
</td>
<td align="left" width="63%">
Obtains an embedded object from a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getend">GetEnd</a>
</td>
<td align="left" width="63%">
Returns an anchor positioned at the end of the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getformattedtext">GetFormattedText</a>
</td>
<td align="left" width="63%">
Returns formatted text information from a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getscreenext">GetScreenExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box screen coordinates of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Returns the offset of a text selection in a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getstart">GetStart</a>
</td>
<td align="left" width="63%">
Returns an anchor positioned at the start of the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the document status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-gettext">GetText</a>
</td>
<td align="left" width="63%">
Returns information about text at a specified anchor position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-gettextext">GetTextExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of a range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getwnd">GetWnd</a>
</td>
<td align="left" width="63%">
Returns the handle to a window that corresponds to the current text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-insertembedded">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an IDataObject data object into a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-insertembeddedatselection">InsertEmbeddedAtSelection</a>
</td>
<td align="left" width="63%">
Inserts an IDataObject object at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-inserttextatselection">InsertTextAtSelection</a>
</td>
<td align="left" width="63%">
Inserts text at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-queryinsert">QueryInsert</a>
</td>
<td align="left" width="63%">
Determines whether the specified start and end anchors are valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-queryinsertembedded">QueryInsertEmbedded</a>
</td>
<td align="left" width="63%">
Determines whether the document can accept an embedded object through the InsertEmbedded or InsertEmbeddedAtSelection methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestattrsatposition">RequestAttrsAtPosition</a>
</td>
<td align="left" width="63%">
Obtains the attributes at the specified anchor location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition">RequestAttrsTransitioningAtPosition</a>
</td>
<td align="left" width="63%">
Obtains a list of attributes that begin or end at the specified anchor location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestlock">RequestLock</a>
</td>
<td align="left" width="63%">
Used by the TSF manager to provide a document lock in order to modify the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestsupportedattrs">RequestSupportedAttrs</a>
</td>
<td align="left" width="63%">
Obtains the supported attributes of a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-retrieverequestedattrs">RetrieveRequestedAttrs</a>
</td>
<td align="left" width="63%">
Returns the attributes obtained by the RequestAttrsAtPosition, RequestAttrsTransitioningAtPosition, or RequestSupportedAttrs methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-setselection">SetSelection</a>
</td>
<td align="left" width="63%">
Selects text within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-settext">SetText</a>
</td>
<td align="left" width="63%">
Sets the text selection between two supplied anchor locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-unadvisesink">UnadviseSink</a>
</td>
<td align="left" width="63%">
Called by an application to indicate that it no longer requires notifications from the TSF manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/ms971350(v=msdn.10)">Microsoft Active Accessibility</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>
 

 

