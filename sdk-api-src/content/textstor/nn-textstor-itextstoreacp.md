---
UID: NN:textstor.ITextStoreACP
title: ITextStoreACP
author: windows-sdk-content
description: The ITextStoreACP interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF.
old-location: tsf\itextstoreacp.htm
tech.root: TSF
ms.assetid: 21e011f7-6791-4eb9-85c9-18bd10107119
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITextStoreACP, ITextStoreACP interface [Text Services Framework], ITextStoreACP interface [Text Services Framework],described, _tsf_itextstoreacp_ref, textstor/ITextStoreACP, tsf.itextstoreacp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreACP interface


## -description


The <b>ITextStoreACP</b> interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF. An application can obtain an instance of this interface with a call to the <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> method. The interface ID is IID_ITextStoreACP.

This interface exposes text stores through an application character position (ACP) format. Applications that use an anchor-based format should use <a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACP</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextStoreACP</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/aadf54e4-25ba-4280-a184-e1d2a2594c3c">AdviseSink</a>
</td>
<td align="left" width="63%">
Identifies the sink interface of the TSF manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5917958-150e-48a5-9d0d-67240a88c232">FindNextAttrTransition</a>
</td>
<td align="left" width="63%">
Determines the character position where an attribute transition occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">GetACPFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point in screen coordinates to an application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7739674e-9524-4530-900c-6e7facc3254f">GetActiveView</a>
</td>
<td align="left" width="63%">
Returns a TsViewCookie data type that specifies the current active view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82904a96-70ec-4ceb-a3c4-5d48c801a9ef">GetEmbedded</a>
</td>
<td align="left" width="63%">
Obtains an embedded object from a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/741ec23f-9d73-40ee-af94-f9a18bbb8e87">GetEndACP</a>
</td>
<td align="left" width="63%">
Returns the number of characters in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c4e6f8d-d7c6-455d-8efe-7da8dfdd9c4b">GetFormattedText</a>
</td>
<td align="left" width="63%">
Returns formatted text information about a specified text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd542dd1-79a5-47ec-a563-cd37a8c36b1a">GetScreenExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2052daf-4168-4266-ae8d-a09ecbfeb422">GetSelection</a>
</td>
<td align="left" width="63%">
Returns the character position of a text selection in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ed040ac-8584-4f09-9af8-218b5cd33765">GetStatus</a>
</td>
<td align="left" width="63%">
Used by the application to obtain the document status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3788e8f-ddb8-4ad6-971c-e9c1f6a21f88">GetText</a>
</td>
<td align="left" width="63%">
Returns information about text at a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d621e96b-d357-4468-8a89-89445fb1ca9e">GetTextExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the text at a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fb49702-4e0e-4e8c-9227-83c0b014f5f2">GetWnd</a>
</td>
<td align="left" width="63%">
Returns the handle to a window that corresponds to the current document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d1612ee-1eb2-44c1-921e-a84af56a0790">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an object into a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a2ecd77-a99e-4476-8485-a44aa88cf563">InsertEmbeddedAtSelection</a>
</td>
<td align="left" width="63%">
Inserts an IDataObject object at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b57ad8da-6f79-4d27-96e0-608cbcaae826">InsertTextAtSelection</a>
</td>
<td align="left" width="63%">
Inserts text at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e02846a2-d50c-4f1e-b44b-1dfa0bf50442">QueryInsert</a>
</td>
<td align="left" width="63%">
Called by an application to determine if the document can accept text at the selection or insertion point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1cf6162-da57-4b8a-beca-fb1ec390c577">QueryInsertEmbedded</a>
</td>
<td align="left" width="63%">
Determines if the document can accept an embedded object through the ITextStoreACP::InsertEmbedded or the ITextStoreACP::InsertEmbeddedAtSelection methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39eb59cd-ec55-4057-8cf1-0203b6e6c82b">RequestAttrsAtPosition</a>
</td>
<td align="left" width="63%">
Obtains the attributes at the specified application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffd27e9b-3281-45a9-84f2-d09103689ced">RequestAttrsTransitioningAtPosition</a>
</td>
<td align="left" width="63%">
Obtains a list of attributes that begin or end at the specified application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddd2b1f4-47de-4e87-be94-eea694ecd1b8">RequestLock</a>
</td>
<td align="left" width="63%">
Called by the TSF manager to provide a document lock so that the TSF manager can modify the document. This method calls the ITextStoreACPSink::OnLockGranted method to create the document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/243cd002-c882-4ce9-b528-1a2229c46f4a">RequestSupportedAttrs</a>
</td>
<td align="left" width="63%">
Obtains the supported attributes of a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cd34ca5-6561-4161-beac-98248f0415f6">RetrieveRequestedAttrs</a>
</td>
<td align="left" width="63%">
Returns the attributes obtained by the ITextStoreACP::RequestAttrsAtPosition, TextStoreACP::RequestAttrsTransitioningAtPosition, or the ITextStoreACP::RequestSupportedAttrs methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">SetSelection</a>
</td>
<td align="left" width="63%">
Selects text within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aebeb6bc-7791-4c45-8563-eec6a738bd63">SetText</a>
</td>
<td align="left" width="63%">
Sets the text selection to the supplied character positions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11445652-e349-46a4-8887-1d1127e16275">UnadviseSink</a>
</td>
<td align="left" width="63%">
Called by the application to indicate that the application no longer requires notifications from the TSF manager.

</td>
</tr>
</table> 


## -see-also




<a href="_COM_IUnknown">IUnknown</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

