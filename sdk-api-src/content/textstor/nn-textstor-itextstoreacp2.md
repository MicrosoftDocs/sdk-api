---
UID: NN:textstor.ITextStoreACP2
title: ITextStoreACP2 (textstor.h)
description: The ITextStoreACP2 interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF.helpviewer_keywords: ["ITextStoreACP2","ITextStoreACP2 interface [Text Services Framework]","ITextStoreACP2 interface [Text Services Framework]","described","textstor/ITextStoreACP2","tsf.itextstoreacp2"]
old-location: tsf\itextstoreacp2.htm
tech.root: TSF
ms.assetid: c256f1c2-6b67-4417-8707-3490a2c5cb55
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2, ITextStoreACP2 interface [Text Services Framework], ITextStoreACP2 interface [Text Services Framework],described, textstor/ITextStoreACP2, tsf.itextstoreacp2
f1_keywords:
- textstor/ITextStoreACP2
dev_langs:
- c++
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- Msctf.dll
api_name:
- ITextStoreACP2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextStoreACP2 interface


## -description


The <b>ITextStoreACP2</b> interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF. An application can obtain an instance of this interface with a call to the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">CreateContext</a> method. The interface ID is <b>IID_ITextStoreACP2</b>.

This interface exposes text stores through an application character position (ACP) format. Applications that use an anchor-based format should use <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACP2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACP2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoreACP2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-advisesink">AdviseSink</a>
</td>
<td align="left" width="63%">
Installs a new advise sink from the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a> interface or modifies an existing advise sink. The sink interface is specified by the <i>punk</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-findnextattrtransition">FindNextAttrTransition</a>
</td>
<td align="left" width="63%">
Determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getacpfrompoint">GetACPFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point in screen coordinates to an application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getactiveview">GetActiveView</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://docs.microsoft.com/windows/desktop/TSF/tsviewcookie">TsViewCookie</a> that represents the current active view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getembedded">GetEmbedded</a>
</td>
<td align="left" width="63%">
Gets an embedded document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getendacp">GetEndACP</a>
</td>
<td align="left" width="63%">
Gets the number of characters in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getformattedtext">GetFormattedText</a>
</td>
<td align="left" width="63%">
Gets formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getscreenext">GetScreenExt</a>
</td>
<td align="left" width="63%">
Gets the bounding box screen coordinates of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the document status. The document status is returned through the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-gettext">GetText</a>
</td>
<td align="left" width="63%">
Gets info about text at a specified character position. This method returns the visible and hidden text and indicates if embedded data is attached to the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-gettextext">GetTextExt</a>
</td>
<td align="left" width="63%">
Gets the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-insertembedded">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an embedded object at the specified character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-insertembeddedatselection">InsertEmbeddedAtSelection</a>
</td>
<td align="left" width="63%">
Inserts an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> at the insertion point or selection. The client that calls this method must have a read/write lock before inserting an <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembeddedatselection">IDataObject</a> object into the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-inserttextatselection">InsertTextAtSelection</a>
</td>
<td align="left" width="63%">
Inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-queryinsert">QueryInsert</a>
</td>
<td align="left" width="63%">
Determines whether the specified start and end character positions are valid. Use this method to adjust an edit to a document before executing the edit. The method must not return values outside the range of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-queryinsertembedded">QueryInsertEmbedded</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the specified object can be inserted into the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-requestattrsatposition">RequestAttrsAtPosition</a>
</td>
<td align="left" width="63%">
Gets text attributes at the specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-requestattrstransitioningatposition">RequestAttrsTransitioningAtPosition</a>
</td>
<td align="left" width="63%">
Gets text attributes transitioning at the specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-requestlock">RequestLock</a>
</td>
<td align="left" width="63%">
Called by the TSF manager to provide a document lock in order to modify the document. This method calls the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">OnLockGranted</a> method to create the document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-requestsupportedattrs">RequestSupportedAttrs</a>
</td>
<td align="left" width="63%">
Get the attributes that are supported in the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-retrieverequestedattrs">RetrieveRequestedAttrs</a>
</td>
<td align="left" width="63%">
Gets the attributes returned by a call to an attribute request method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-setselection">SetSelection</a>
</td>
<td align="left" width="63%">
Selects text within the document. The application must have a read/write lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-settext">SetText</a>
</td>
<td align="left" width="63%">
Sets the text selection to the supplied character positions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-unadvisesink">UnadviseSink</a>
</td>
<td align="left" width="63%">
Called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.

</td>
</tr>
</table> 

