---
UID: NF:docobj.IOleDocumentView.Open
title: IOleDocumentView::Open
author: windows-sdk-content
description: Displays a document view in a separate pop-up window. The semantics are equivalent to IOleObject::DoVerb with OLEIVERB_OPEN.
old-location: com\ioledocumentview_open.htm
old-project: com
ms.assetid: 46f801ae-ae03-4567-9442-cf3fbb6d06d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOleDocumentView interface [COM],Open method, IOleDocumentView.Open, IOleDocumentView::Open, Open, Open method [COM], Open method [COM],IOleDocumentView interface, _ole_ioledocumentview_open, com.ioledocumentview_open, docobj/IOleDocumentView::Open
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: docobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DOCMISC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DocObj.h
api_name:
 - IOleDocumentView.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IOleDocumentView::Open


## -description


Displays a document view in a separate pop-up window. The semantics are equivalent to <a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">IOleObject::DoVerb</a> with OLEIVERB_OPEN.


## -parameters






## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory  available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The document object that owns this view does not support separate window activation.

</td>
</tr>
</table>
 




## -remarks



A user viewing a document object in a container application such as a browser or "binder" may want to see two or more views or documents at once. Because the browser displays only one view at a time, the container needs a way to ask the other views or documents to display themselves, as required, in separate windows. The <b>IOleDocumentView::Open</b> method provides that way.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A successful call to <b>IOleDocumentView::Open</b> should be followed by a call to <a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a> to hide the window or to show the window and bring it to the foreground. While the view is active in its separate window, a container can show or hide the window as many times as it may require.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
A document object indicates that it does not support activation in a separate window by setting the <a href="https://msdn.microsoft.com/e52e022e-dd82-42f0-a3dd-2730ad80613c">DOCMISC</a>_CANTOPENEDIT status flag and returning E_NOTIMPL to containers that call this method.

Implementation consists mainly of the view object calling its own <a href="https://msdn.microsoft.com/174a8bde-0795-4d4d-a294-7708c7d1823a">IOleInPlaceObject::InPlaceDeactivate</a> method, which leaves the document object in a running state but without in-place activation. The document object's user interface is not visible until the container calls <a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a> (see Notes to Callers above).




## -see-also




<a href="https://msdn.microsoft.com/07948c08-f047-4ae0-a41b-5410b4bbf4d6">IOleDocumentView</a>



<a href="https://msdn.microsoft.com/d2f443de-929e-4bd4-bfb3-2a28c119c176">IOleDocumentView::CloseView</a>



<a href="https://msdn.microsoft.com/eecc0230-0713-40e9-913c-c51b8a905575">IOleDocumentView::Show</a>



<a href="https://msdn.microsoft.com/df92366c-89b3-44b3-bea0-1b6deb321fe4">IOleDocumentView::UIActivate</a>



<a href="https://msdn.microsoft.com/174a8bde-0795-4d4d-a294-7708c7d1823a">IOleInPlaceObject::InPlaceDeactivate</a>



<a href="https://msdn.microsoft.com/6d37e022-8c19-48b3-affb-e0eca19b5e05">IOleInPlaceSite</a>



<a href="https://msdn.microsoft.com/e5744911-1ea6-4482-988d-8def16229f4c">IOleInPlaceSite::OnInPlaceActivate</a>
 

 

