---
UID: NN:oleidl.IOleObject
title: IOleObject
author: windows-sdk-content
description: Serves as the principal means by which an embedded object provides basic functionality to, and communicates with, its container.
old-location: com\ioleobject.htm
old-project: com
ms.assetid: 58b32c87-39b6-4d64-9174-cf798ed302c2
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IOleObject, IOleObject interface [COM], IOleObject interface [COM],described, _ole_ioleobject, com.ioleobject, oleidl/IOleObject
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
 - IOleObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: ADAM
---

# IOleObject interface


## -description


Serves as the principal means by which an embedded object provides basic functionality to, and communicates 
    with, its container.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleObject</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOleObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">Advise</a>
</td>
<td align="left" width="63%">
Establishes an advisory connection between a compound document object and the calling object's advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Changes an embedded object from the running to the loaded state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fabd6a0a-7b0c-4c99-af22-8b117addd5f7">DoVerb</a>
</td>
<td align="left" width="63%">
Requests that an object perform an action in response to an end-user's action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc">EnumAdvise</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an enumerator that can be used to enumerate the advisory connections registered for an 
       object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">EnumVerbs</a>
</td>
<td align="left" width="63%">
Exposes a pull-down menu listing the verbs available for an object in ascending order by verb number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf26b989-445c-48d3-b279-29e4cef0ad97">GetClientSite</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an embedded object's client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49f6b26c-76e1-4519-920b-e05279f23112">GetClipboardData</a>
</td>
<td align="left" width="63%">
Retrieves a data object containing the current contents of the embedded object on which this method is 
       called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/babaf55e-6c43-48d8-ad13-1333e29a3e1d">GetExtent</a>
</td>
<td align="left" width="63%">
Retrieves a running object's current display area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c5e9f73-8eec-48e0-a172-4d3d49e56071">GetMiscStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of an object at creation and loading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b81ca75-31d8-45d6-8b36-663c5f19341c">GetMoniker</a>
</td>
<td align="left" width="63%">
Retrieves an embedded object's moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b3c0292-0476-4f56-abd2-2f3a82195c67">GetUserClassID</a>
</td>
<td align="left" width="63%">
Retrieves an object's class identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ffffa01-d118-4955-84d1-a4659ba9ddc9">GetUserType</a>
</td>
<td align="left" width="63%">
Retrieves the user-type name of an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bbda602-4421-4f79-a33a-63ded9a8bf90">InitFromData</a>
</td>
<td align="left" width="63%">
Initializes a newly created object with data from the specified data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74203a74-c5dd-4a98-9223-1dc54c9d4399">IsUpToDate</a>
</td>
<td align="left" width="63%">
Checks whether an object is up to date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6690b5a3-bada-496c-89cb-a9ae1fc9dfb0">SetClientSite</a>
</td>
<td align="left" width="63%">
Informs an embedded object of its client site within its container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/655ba4ea-941d-4389-9ee8-756dfa3c5448">SetColorScheme</a>
</td>
<td align="left" width="63%">
Specifies the color palette that the object application should use when it edits the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1960095-7c9a-4058-aef1-f31e3d6e3509">SetExtent</a>
</td>
<td align="left" width="63%">
Sets the extent of object's display area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38cccb3d-e198-4996-991b-6c56451d25e3">SetHostNames</a>
</td>
<td align="left" width="63%">
Provides an object with the names of its container application and the compound document in which it is 
       embedded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1313cd9a-757d-4716-abac-027cff9fee03">SetMoniker</a>
</td>
<td align="left" width="63%">
Notifies an object of its container's moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3d63a75-30b0-4fe5-9a1d-c70820583765">Unadvise</a>
</td>
<td align="left" width="63%">
Deletes a previously established advisory connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Updates an object handler's or link object's data or view caches.

</td>
</tr>
</table> 

