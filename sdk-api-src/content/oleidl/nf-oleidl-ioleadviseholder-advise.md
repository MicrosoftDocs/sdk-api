---
UID: NF:oleidl.IOleAdviseHolder.Advise
title: IOleAdviseHolder::Advise
author: windows-sdk-content
description: Establishes an advisory connection between an OLE object and the calling object's advise sink. Through that sink, the calling object can receive notification when the OLE object is renamed, saved, or closed.
old-location: com\ioleadviseholder_advise.htm
old-project: com
ms.assetid: 60bbb555-7d01-49cb-b7b3-9dc905066f94
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Advise, Advise method [COM], Advise method [COM],IOleAdviseHolder interface, IOleAdviseHolder interface [COM],Advise method, IOleAdviseHolder.Advise, IOleAdviseHolder::Advise, _ole_ioleadviseholder_advise, com.ioleadviseholder_advise, oleidl/IOleAdviseHolder::Advise
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
 - IOleAdviseHolder.Advise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleAdviseHolder::Advise


## -description


Establishes an advisory connection between an OLE object and the calling object's advise sink. Through that sink, the calling object can receive notification when the OLE object is renamed, saved, or closed.


## -parameters




### -param pAdvise [in]

A pointer to the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface on the advisory sink that should be informed of changes.


### -param pdwConnection [out]

A pointer to a token that can be passed to the <a href="https://msdn.microsoft.com/620bc43f-dfc7-48b7-a574-ca7287ffa42f">IOleAdviseHolder::Unadvise</a> method to delete the advisory connection. The calling object is responsible for calling both <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> and <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on this pointer.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface pointer is invalid.

</td>
</tr>
</table>
 




## -remarks



Containers, object handlers, and link objects all create advise sinks to receive notification of changes in compound-document objects of interest, such as embedded or linked objects. OLE objects of interest to these objects must implement the <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface, which includes several advisory methods, including <a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a>. A call to this method must set up an advisory connection with any advise sink that calls it, and maintain each connection until it is closed. It must be able to handle more than one advisory connection at a time.

<b>IOleAdviseHolder::Advise</b> is intended to be used to simplify the implementation of <a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a>. You can get a pointer to the OLE implementation of IOleAdviseHolder by calling <a href="https://msdn.microsoft.com/f76e074e-6814-4735-9417-d5970e73089f">CreateOleAdviseHolder</a>, and then, to implement <b>IOleObject::Advise</b>, just delegate the call to <b>IOleAdviseHolder::Advise</b>. Other <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a> methods are intended to implement other <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> advisory methods.

If the attempt to establish an advisory connection is successful, the object receiving the call returns a nonzero value through <i>pdwConnection</i>. If the attempt fails, the object returns a zero. To delete an advisory connection, the object with the advise sink passes this nonzero token back to the object by calling <b>IOleAdviseHolder::Advise</b>.




## -see-also




<a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a>



<a href="https://msdn.microsoft.com/80a9ccd8-f89a-40c4-8b99-38536409cf26">IOleAdviseHolder::EnumAdvise</a>



<a href="https://msdn.microsoft.com/620bc43f-dfc7-48b7-a574-ca7287ffa42f">IOleAdviseHolder::Unadvise</a>



<a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a>
 

 

