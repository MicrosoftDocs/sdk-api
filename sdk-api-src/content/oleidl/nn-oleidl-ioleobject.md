---
UID: NN:oleidl.IOleObject
title: IOleObject (oleidl.h)
description: Serves as the principal means by which an embedded object provides basic functionality to, and communicates with, its container.
helpviewer_keywords: ["IOleObject","IOleObject interface [COM]","IOleObject interface [COM]","described","_ole_ioleobject","com.ioleobject","oleidl/IOleObject"]
old-location: com\ioleobject.htm
tech.root: com
ms.assetid: 58b32c87-39b6-4d64-9174-cf798ed302c2
ms.date: 12/05/2018
ms.keywords: IOleObject, IOleObject interface [COM], IOleObject interface [COM],described, _ole_ioleobject, com.ioleobject, oleidl/IOleObject
f1_keywords:
- oleidl/IOleObject
dev_langs:
- c++
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
- IOleObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleObject interface


## -description


Serves as the principal means by which an embedded object provides basic functionality to, and communicates 
    with, its container.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleObject</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">Advise</a>
</td>
<td align="left" width="63%">
Establishes an advisory connection between a compound document object and the calling object's advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">Close</a>
</td>
<td align="left" width="63%">
Changes an embedded object from the running to the loaded state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">DoVerb</a>
</td>
<td align="left" width="63%">
Requests that an object perform an action in response to an end-user's action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumadvise">EnumAdvise</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an enumerator that can be used to enumerate the advisory connections registered for an 
       object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">EnumVerbs</a>
</td>
<td align="left" width="63%">
Exposes a pull-down menu listing the verbs available for an object in ascending order by verb number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getclientsite">GetClientSite</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an embedded object's client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getclipboarddata">GetClipboardData</a>
</td>
<td align="left" width="63%">
Retrieves a data object containing the current contents of the embedded object on which this method is 
       called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">GetExtent</a>
</td>
<td align="left" width="63%">
Retrieves a running object's current display area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmiscstatus">GetMiscStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of an object at creation and loading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmoniker">GetMoniker</a>
</td>
<td align="left" width="63%">
Retrieves an embedded object's moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getuserclassid">GetUserClassID</a>
</td>
<td align="left" width="63%">
Retrieves an object's class identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">GetUserType</a>
</td>
<td align="left" width="63%">
Retrieves the user-type name of an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-initfromdata">InitFromData</a>
</td>
<td align="left" width="63%">
Initializes a newly created object with data from the specified data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-isuptodate">IsUpToDate</a>
</td>
<td align="left" width="63%">
Checks whether an object is up to date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">SetClientSite</a>
</td>
<td align="left" width="63%">
Informs an embedded object of its client site within its container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setcolorscheme">SetColorScheme</a>
</td>
<td align="left" width="63%">
Specifies the color palette that the object application should use when it edits the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setextent">SetExtent</a>
</td>
<td align="left" width="63%">
Sets the extent of object's display area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-sethostnames">SetHostNames</a>
</td>
<td align="left" width="63%">
Provides an object with the names of its container application and the compound document in which it is 
       embedded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">SetMoniker</a>
</td>
<td align="left" width="63%">
Notifies an object of its container's moniker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Deletes a previously established advisory connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">Update</a>
</td>
<td align="left" width="63%">
Updates an object handler's or link object's data or view caches.

</td>
</tr>
</table> 

