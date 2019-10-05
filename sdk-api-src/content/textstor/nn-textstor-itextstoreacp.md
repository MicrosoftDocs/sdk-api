---
UID: NN:textstor.ITextStoreACP
title: ITextStoreACP (textstor.h)
author: windows-sdk-content
description: The ITextStoreACP interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF.
old-location: tsf\itextstoreacp.htm
tech.root: TSF
ms.assetid: 21e011f7-6791-4eb9-85c9-18bd10107119
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoreACP, ITextStoreACP interface [Text Services Framework], ITextStoreACP interface [Text Services Framework],described, _tsf_itextstoreacp_ref, textstor/ITextStoreACP, tsf.itextstoreacp
ms.topic: interface
f1_keywords: 
 - "textstor/ITextStoreACP"
dev_langs:
 - c++
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreACP interface


## -description


The <b>ITextStoreACP</b> interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF. An application can obtain an instance of this interface with a call to the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> method. The interface ID is IID_ITextStoreACP.

This interface exposes text stores through an application character position (ACP) format. Applications that use an anchor-based format should use <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACP</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoreACP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">AdviseSink</a>
</td>
<td align="left" width="63%">
Identifies the sink interface of the TSF manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-findnextattrtransition">FindNextAttrTransition</a>
</td>
<td align="left" width="63%">
Determines the character position where an attribute transition occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">GetACPFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point in screen coordinates to an application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getactiveview">GetActiveView</a>
</td>
<td align="left" width="63%">
Returns a TsViewCookie data type that specifies the current active view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded">GetEmbedded</a>
</td>
<td align="left" width="63%">
Obtains an embedded object from a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getendacp">GetEndACP</a>
</td>
<td align="left" width="63%">
Returns the number of characters in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getformattedtext">GetFormattedText</a>
</td>
<td align="left" width="63%">
Returns formatted text information about a specified text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getscreenext">GetScreenExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Returns the character position of a text selection in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Used by the application to obtain the document status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext">GetText</a>
</td>
<td align="left" width="63%">
Returns information about text at a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">GetTextExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the text at a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getwnd">GetWnd</a>
</td>
<td align="left" width="63%">
Returns the handle to a window that corresponds to the current document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an object into a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembeddedatselection">InsertEmbeddedAtSelection</a>
</td>
<td align="left" width="63%">
Inserts an IDataObject object at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-inserttextatselection">InsertTextAtSelection</a>
</td>
<td align="left" width="63%">
Inserts text at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-queryinsert">QueryInsert</a>
</td>
<td align="left" width="63%">
Called by an application to determine if the document can accept text at the selection or insertion point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-queryinsertembedded">QueryInsertEmbedded</a>
</td>
<td align="left" width="63%">
Determines if the document can accept an embedded object through the ITextStoreACP::InsertEmbedded or the ITextStoreACP::InsertEmbeddedAtSelection methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestattrsatposition">RequestAttrsAtPosition</a>
</td>
<td align="left" width="63%">
Obtains the attributes at the specified application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition">RequestAttrsTransitioningAtPosition</a>
</td>
<td align="left" width="63%">
Obtains a list of attributes that begin or end at the specified application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestlock">RequestLock</a>
</td>
<td align="left" width="63%">
Called by the TSF manager to provide a document lock so that the TSF manager can modify the document. This method calls the ITextStoreACPSink::OnLockGranted method to create the document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestsupportedattrs">RequestSupportedAttrs</a>
</td>
<td align="left" width="63%">
Obtains the supported attributes of a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-retrieverequestedattrs">RetrieveRequestedAttrs</a>
</td>
<td align="left" width="63%">
Returns the attributes obtained by the ITextStoreACP::RequestAttrsAtPosition, TextStoreACP::RequestAttrsTransitioningAtPosition, or the ITextStoreACP::RequestSupportedAttrs methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-setselection">SetSelection</a>
</td>
<td align="left" width="63%">
Selects text within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-settext">SetText</a>
</td>
<td align="left" width="63%">
Sets the text selection to the supplied character positions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-unadvisesink">UnadviseSink</a>
</td>
<td align="left" width="63%">
Called by the application to indicate that the application no longer requires notifications from the TSF manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/text-stores">Text Stores</a>
 

 

