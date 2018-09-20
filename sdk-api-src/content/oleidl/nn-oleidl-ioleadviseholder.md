---
UID: NN:oleidl.IOleAdviseHolder
title: IOleAdviseHolder
author: windows-sdk-content
description: Manages advisory connections and compound document notifications in an object server.
old-location: com\ioleadviseholder.htm
tech.root: com
ms.assetid: 680afee7-2bee-4d54-ae0b-3e4e0deb622f
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IOleAdviseHolder, IOleAdviseHolder interface [COM], IOleAdviseHolder interface [COM],described, _ole_ioleadviseholder, com.ioleadviseholder, oleidl/IOleAdviseHolder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleAdviseHolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleAdviseHolder interface


## -description


Manages advisory connections and compound document notifications in an object server. Its methods are intended to be used to implement the advisory methods of <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>. <b>IOleAdviseHolder</b> is implemented on an advise holder object. Its methods establish and delete advisory connections from the object managed by the server to the object's container, which must contain an advise sink (support the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface). The advise holder object must also keep track of which advise sinks are interested in which notifications and pass along the notifications as appropriate.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleAdviseHolder</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleAdviseHolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleAdviseHolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60bbb555-7d01-49cb-b7b3-9dc905066f94">Advise</a>
</td>
<td align="left" width="63%">
Establishes an advisory connection between an OLE object and the calling object's advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80a9ccd8-f89a-40c4-8b99-38536409cf26">EnumAdvise</a>
</td>
<td align="left" width="63%">
Creates an enumerator that can be used to enumerate the advisory connections currently established for an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4efa947-d357-432c-9585-b00b19551ad6">SendOnClose</a>
</td>
<td align="left" width="63%">
Sends notification to all advisory sinks currently registered with the advise holder that the object has closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64e44cab-b618-49af-bf0e-966b9eaa198a">SendOnRename</a>
</td>
<td align="left" width="63%">
Sends notification to all advisory sinks currently registered with the advise holder that the name of object has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b64ceaf7-45ba-4a66-a5cf-aec352472d3d">SendOnSave</a>
</td>
<td align="left" width="63%">
Sends notification to all advisory sinks currently registered with the advise holder that the object has been saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/620bc43f-dfc7-48b7-a574-ca7287ffa42f">Unadvise</a>
</td>
<td align="left" width="63%">
Deletes a previously established advisory connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f76e074e-6814-4735-9417-d5970e73089f">CreateOleAdviseHolder</a>



<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>
 

 

