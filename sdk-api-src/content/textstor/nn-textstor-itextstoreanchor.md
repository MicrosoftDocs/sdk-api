---
UID: NN:textstor.ITextStoreAnchor
title: ITextStoreAnchor
author: windows-sdk-content
description: The ITextStoreAnchor interface is implemented by a Microsoft Active Accessibility client and is used by the TSF manager to manipulate text streams.
old-location: tsf\itextstoreanchor.htm
tech.root: TSF
ms.assetid: 62730a6d-4dc8-4207-9818-ab95e6537854
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITextStoreAnchor, ITextStoreAnchor interface [Text Services Framework], ITextStoreAnchor interface [Text Services Framework],described, _tsf_itextstoreanchor_ref, textstor/ITextStoreAnchor, tsf.itextstoreanchor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor interface


## -description


The ITextStoreAnchor interface is implemented by a <a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Microsoft Active Accessibility</a> client and is used by the TSF manager to manipulate text streams. <a href="https://msdn.microsoft.com/7488e29e-3409-4db3-98b4-f3438ad7c94e">Ranges</a> of text within a stream are delimited by <a href="https://msdn.microsoft.com/en-us/library/ms629023(v=VS.85).aspx">anchor</a> objects. these anchor objects are exposed and manipulated by the <a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a> interface.

An application can obtain an instance of this interface with <a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Microsoft Active Accessibility</a>. The interface ID is IID_ITextStoreAnchor.

To use the application character position (ACP) model for text manipulation, use <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> instead.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreAnchor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextStoreAnchor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a2196d1c-b03e-44b4-b695-970feddb8ce5">AdviseSink</a>
</td>
<td align="left" width="63%">
Installs a new advise sink or modifies an existing advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bb21a4a-047e-4347-93b3-9c41cd2c20b7">FindNextAttrTransition</a>
</td>
<td align="left" width="63%">
Finds the location in the text stream where a transition occurs in an attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1940cac-7295-41c5-bd26-8be1d1fa4da9">GetActiveView</a>
</td>
<td align="left" width="63%">
Returns a TsViewCookie data type that specifies the current active view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5567b53e-540e-41ce-b890-f2e4c5b06c57">GetAnchorFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point in screen coordinates to an anchor positioned at a corresponding location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/212286e1-aafa-4368-8dd3-45a0d4c6ecb9">GetEmbedded</a>
</td>
<td align="left" width="63%">
Obtains an embedded object from a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c510900-bcff-4ea1-a8f3-95b6f47b3432">GetEnd</a>
</td>
<td align="left" width="63%">
Returns an anchor positioned at the end of the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b104b0a-b900-4acb-801e-d9716e3a0146">GetFormattedText</a>
</td>
<td align="left" width="63%">
Returns formatted text information from a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e1b446e-935f-492a-b168-8d1b60868d72">GetScreenExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box screen coordinates of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df1b21b7-b539-4546-96be-243a8e7ea75a">GetSelection</a>
</td>
<td align="left" width="63%">
Returns the offset of a text selection in a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/431ca3b0-920b-4a4e-b475-32175555a789">GetStart</a>
</td>
<td align="left" width="63%">
Returns an anchor positioned at the start of the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61192268-5a5f-4caa-bdb8-799ee4aea24e">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the document status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd3f91df-b107-4284-8435-d859c843555f">GetText</a>
</td>
<td align="left" width="63%">
Returns information about text at a specified anchor position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8e21544-e5d2-4048-93aa-82a87562a70a">GetTextExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of a range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e77b5218-45e4-4fe1-a41f-1d7b5887ba30">GetWnd</a>
</td>
<td align="left" width="63%">
Returns the handle to a window that corresponds to the current text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/414842cc-7c3e-4f5c-93ac-3bd0eda5293e">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an IDataObject data object into a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22c804b9-e260-4a8a-bbb3-fcc81fa97c7a">InsertEmbeddedAtSelection</a>
</td>
<td align="left" width="63%">
Inserts an IDataObject object at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5cb512a-d9f5-451f-b6cb-2020ba32e855">InsertTextAtSelection</a>
</td>
<td align="left" width="63%">
Inserts text at the insertion point or selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/953b3f9c-63b7-4d62-accb-b07acfa97432">QueryInsert</a>
</td>
<td align="left" width="63%">
Determines whether the specified start and end anchors are valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/722506fa-db83-49d3-9434-a4ad7b797ce2">QueryInsertEmbedded</a>
</td>
<td align="left" width="63%">
Determines whether the document can accept an embedded object through the InsertEmbedded or InsertEmbeddedAtSelection methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0f20507-005b-409d-90d5-5817b7d95f19">RequestAttrsAtPosition</a>
</td>
<td align="left" width="63%">
Obtains the attributes at the specified anchor location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0f43237-8c26-4e0c-8717-908884229b7b">RequestAttrsTransitioningAtPosition</a>
</td>
<td align="left" width="63%">
Obtains a list of attributes that begin or end at the specified anchor location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">RequestLock</a>
</td>
<td align="left" width="63%">
Used by the TSF manager to provide a document lock in order to modify the text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab81d79d-e991-4c2d-9fb7-95393e002828">RequestSupportedAttrs</a>
</td>
<td align="left" width="63%">
Obtains the supported attributes of a text stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">RetrieveRequestedAttrs</a>
</td>
<td align="left" width="63%">
Returns the attributes obtained by the RequestAttrsAtPosition, RequestAttrsTransitioningAtPosition, or RequestSupportedAttrs methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce301fa4-d1dd-4470-b8b5-fc944afdc621">SetSelection</a>
</td>
<td align="left" width="63%">
Selects text within the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03beac03-cd09-4e03-b700-d96741e4932b">SetText</a>
</td>
<td align="left" width="63%">
Sets the text selection between two supplied anchor locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01ddc659-0ed9-41e9-bde9-92aad9d74716">UnadviseSink</a>
</td>
<td align="left" width="63%">
Called by an application to indicate that it no longer requires notifications from the TSF manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/ms971350(v=MSDN.10).aspx">Microsoft Active Accessibility</a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie
      </a>
 

 

