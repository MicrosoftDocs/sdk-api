---
UID: NF:oleidl.IOleObject.Advise
title: IOleObject::Advise
author: windows-sdk-content
description: Establishes an advisory connection between a compound document object and the calling object's advise sink, through which the calling object receives notification when the compound document object is renamed, saved, or closed.
old-location: com\ioleobject_advise.htm
old-project: com
ms.assetid: 6a68c9e9-6e06-4def-89a5-18e184e76a26
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Advise, Advise method [COM], Advise method [COM],IOleObject interface, IOleObject interface [COM],Advise method, IOleObject.Advise, IOleObject::Advise, _ole_ioleobject_advise, com.ioleobject_advise, oleidl/IOleObject::Advise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.redist: 
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
 - IOleObject.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleObject::Advise


## -description


Establishes an advisory connection between a compound document object and the calling object's advise sink, through which the calling object receives notification when the compound document object is renamed, saved, or closed.


## -parameters




### -param pAdvSink [in]

Pointer to the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface on the advise sink of the calling object.


### -param pdwConnection [out]

Pointer to a token that can be passed to <a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a> to delete the advisory connection.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



The <b>IOleObject::Advise</b> method sets up an advisory connection between an object and its container, through which the object informs the container's advise sink of close, save, rename, and link-source change events in the object. A container calls this method, normally as part of initializing an object, to register its advisory sink with the object. In return, the object sends the container compound-document notifications by calling <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> or <a href="https://msdn.microsoft.com/80f55377-8a1e-42b1-8fe0-5896620c8062">IAdviseSink2</a>.

If container and object successfully establish an advisory connection, the object receiving the call returns a nonzero value through <i>pdwConnection</i> to the container. If the attempt to establish an advisory connection fails, the object returns zero. To delete an advisory connection, the container calls <a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a> and passes this nonzero token back to the object.

An object can delegate the job of managing and tracking advisory events to an OLE advise holder, to which you obtain a pointer by calling <a href="https://msdn.microsoft.com/f76e074e-6814-4735-9417-d5970e73089f">CreateOleAdviseHolder</a>. The returned <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a> interface has three methods for sending advisory notifications, as well as <a href="https://msdn.microsoft.com/60bbb555-7d01-49cb-b7b3-9dc905066f94">IOleAdviseHolder::Advise</a>, <a href="https://msdn.microsoft.com/620bc43f-dfc7-48b7-a574-ca7287ffa42f">IOleAdviseHolder::Unadvise</a>, and <a href="https://msdn.microsoft.com/80a9ccd8-f89a-40c4-8b99-38536409cf26">IOleAdviseHolder::EnumAdvise</a> methods that are identical to those for <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>. Calls to <b>IOleObject::Advise</b>, <a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a>, or <a href="https://msdn.microsoft.com/4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc">IOleObject::EnumAdvise</a> are delegated to corresponding methods in the advise holder.

To destroy the advise holder, simply call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on the <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/f76e074e-6814-4735-9417-d5970e73089f">CreateOleAdviseHolder</a>



<a href="https://msdn.microsoft.com/60bbb555-7d01-49cb-b7b3-9dc905066f94">IOleAdviseHolder::Advise</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>



<a href="https://msdn.microsoft.com/4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc">IOleObject::EnumAdvise</a>



<a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">IOleObject::Unadvise</a>
 

 

