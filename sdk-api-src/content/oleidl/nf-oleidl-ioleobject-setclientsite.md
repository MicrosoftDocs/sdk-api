---
UID: NF:oleidl.IOleObject.SetClientSite
title: IOleObject::SetClientSite
author: windows-sdk-content
description: Informs an embedded object of its display location, called a &#0034;client site,&#0034; within its container.
old-location: com\ioleobject_setclientsite.htm
old-project: com
ms.assetid: 6690b5a3-bada-496c-89cb-a9ae1fc9dfb0
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IOleObject interface [COM],SetClientSite method, IOleObject.SetClientSite, IOleObject::SetClientSite, SetClientSite, SetClientSite method [COM], SetClientSite method [COM],IOleObject interface, _ole_ioleobject_setclientsite, com.ioleobject_setclientsite, oleidl/IOleObject::SetClientSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.SetClientSite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleObject::SetClientSite


## -description


Informs an embedded object of its display location, called a "client site," within its container.


## -parameters




### -param pClientSite [in]

Pointer to the <a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a> interface on the container application's client-site.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



Within a compound document, each embedded object has its own client site  â€” the place where it is displayed and through which it receives information about its storage, user interface, and other resources. <b>IOleObject::SetClientSite</b> is the only method enabling an embedded object to obtain a pointer to its client site.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container can notify an object of its client site either at the time the object is created or, subsequently, when the object is initialized.

When creating or loading an object, a container may pass a client-site pointer (along with other arguments) to one of the following helper functions: <a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>, <a href="https://msdn.microsoft.com/98c63646-6617-46b6-8c3e-82d1c4d0adb6">OleCreateFromFile</a>, <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> or <a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a>. These helper functions load an object handler for the new object and call <b>IOleObject::SetClientSite</b> on the container's behalf before returning a pointer to the new object.

Passing a client-site pointer informs the object handler that the client site is ready to process requests. If the client site is unlikely to be ready immediately after the handler is loaded, you may want your container to pass a <b>NULL</b> client-site pointer to the helper function. The <b>NULL</b> pointer says that no client site is available and thereby defers notifying the object handler of the client site until the object is initialized. In response, the helper function returns a pointer to the object, but upon receiving that pointer the container must call <b>IOleObject::SetClientSite</b> as part of initializing the new object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementation consists simply of incrementing the reference count on, and storing, the pointer to the client site.




## -see-also




<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/bf26b989-445c-48d3-b279-29e4cef0ad97">IOleObject::GetClientSite</a>



<a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>



<a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>



<a href="https://msdn.microsoft.com/98c63646-6617-46b6-8c3e-82d1c4d0adb6">OleCreateFromFile</a>



<a href="https://msdn.microsoft.com/f2d8bb2e-5bd1-4991-a80c-ed06bfd5c9f9">OleLoad</a>
 

 

