---
UID: NN:textstor.ITextStoreACP2
title: ITextStoreACP2
author: windows-driver-content
description: The ITextStoreACP2 interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF.
old-location: tsf\itextstoreacp2.htm
old-project: TSF
ms.assetid: c256f1c2-6b67-4417-8707-3490a2c5cb55
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITextStoreACP2, ITextStoreACP2 interface [Text Services Framework], ITextStoreACP2 interface [Text Services Framework],described, textstor/ITextStoreACP2, tsf.itextstoreacp2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITextStoreACP2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP2 interface


## -description


The <b>ITextStoreACP2</b> interface is implemented by the application and is used by the TSF manager to manipulate text streams or text stores in TSF. An application can obtain an instance of this interface with a call to the <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">CreateContext</a> method. The interface ID is <b>IID_ITextStoreACP2</b>.

This interface exposes text stores through an application character position (ACP) format. Applications that use an anchor-based format should use <a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACP2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextStoreACP2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/15fa2f85-3fe8-4e2d-bd3b-a270182adc66">AdviseSink</a>
</td>
<td align="left" width="63%">
Installs a new advise sink from the <a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a> interface or modifies an existing advise sink. The sink interface is specified by the <i>punk</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ccad786-64e0-423c-8b8e-c853123828e5">FindNextAttrTransition</a>
</td>
<td align="left" width="63%">
Determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2907cd34-6ebe-45b4-afd6-8062212c3dc9">GetACPFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point in screen coordinates to an application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38db4fd3-3268-4b3d-9e2c-19d80afeba47">GetActiveView</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie</a> that represents the current active view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e67702-4056-4b29-97a9-441045b29338">GetEmbedded</a>
</td>
<td align="left" width="63%">
Gets an embedded document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61429956-8996-450e-af24-0c91ea974865">GetEndACP</a>
</td>
<td align="left" width="63%">
Gets the number of characters in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0993861d-ef2a-4da5-a564-7559e7c4dcec">GetFormattedText</a>
</td>
<td align="left" width="63%">
Gets formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdc258ab-b692-495c-be76-0b41d75625e2">GetScreenExt</a>
</td>
<td align="left" width="63%">
Gets the bounding box screen coordinates of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f0c6265-7dba-4c59-94f9-36341f05c18d">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the document status. The document status is returned through the <a href="https://msdn.microsoft.com/d27d81f2-8599-4b65-866b-4e8fd2f589f5">TS_STATUS</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>
</td>
<td align="left" width="63%">
Gets info about text at a specified character position. This method returns the visible and hidden text and indicates if embedded data is attached to the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44ede856-f4e7-4d82-8a15-c79a95e4994f">GetTextExt</a>
</td>
<td align="left" width="63%">
Gets the bounding box, in screen coordinates, of the text at a specified character position. The caller must have a read-only lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f5003e0-0d6d-4212-beea-3b2685991749">InsertEmbedded</a>
</td>
<td align="left" width="63%">
Inserts an embedded object at the specified character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/677114a5-8c87-4632-b308-2bb6dedf78c8">InsertEmbeddedAtSelection</a>
</td>
<td align="left" width="63%">
Inserts an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> at the insertion point or selection. The client that calls this method must have a read/write lock before inserting an <a href="https://msdn.microsoft.com/5a2ecd77-a99e-4476-8485-a44aa88cf563">IDataObject</a> object into the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e1e0893-53be-4753-ba49-32e69597a130">InsertTextAtSelection</a>
</td>
<td align="left" width="63%">
Inserts text at the insertion point or selection. A caller must have a read/write lock on the document before inserting text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a1cf233-5185-414a-99c6-2cfdbe07b8c9">QueryInsert</a>
</td>
<td align="left" width="63%">
Determines whether the specified start and end character positions are valid. Use this method to adjust an edit to a document before executing the edit. The method must not return values outside the range of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af67d721-290b-412d-9d99-ea7d6406f33d">QueryInsertEmbedded</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the specified object can be inserted into the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0eb663be-3e70-415b-89cd-7e5a0308e72a">RequestAttrsAtPosition</a>
</td>
<td align="left" width="63%">
Gets text attributes at the specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff1cda58-f02d-4c39-aed5-ebacbef20780">RequestAttrsTransitioningAtPosition</a>
</td>
<td align="left" width="63%">
Gets text attributes transitioning at the specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82254529-3deb-4e69-8571-3f8eaa533459">RequestLock</a>
</td>
<td align="left" width="63%">
Called by the TSF manager to provide a document lock in order to modify the document. This method calls the <a href="https://msdn.microsoft.com/ddedd278-ec28-417e-bce2-cdb74db7b0f3">OnLockGranted</a> method to create the document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce26c2ec-f808-4f59-bc54-b3681b97ad89">RequestSupportedAttrs</a>
</td>
<td align="left" width="63%">
Get the attributes that are supported in the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fff22304-626e-4ae6-ac8c-f4a62ee823c2">RetrieveRequestedAttrs</a>
</td>
<td align="left" width="63%">

      Gets the attributes returned by a call to an attribute request method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ed72ddd-523e-476a-ba4c-bbfef9483015">SetSelection</a>
</td>
<td align="left" width="63%">
Selects text within the document. The application must have a read/write lock on the document before calling this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a00b8273-1690-4cf5-899f-afcb1092bfe8">SetText</a>
</td>
<td align="left" width="63%">
Sets the text selection to the supplied character positions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08c78d99-a6ff-4ac1-9357-77bbae70400f">UnadviseSink</a>
</td>
<td align="left" width="63%">
Called by an application to indicate that it no longer requires notifications from the TSF manager. The TSF manager will release the sink interface and stop notifications.

</td>
</tr>
</table> 

