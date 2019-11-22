---
UID: NN:ocidl.IObjectWithSite
title: IObjectWithSite (ocidl.h)

description: Provides a simple way to support communication between an object and its site in the container.
old-location: com\iobjectwithsite.htm
tech.root: com
ms.assetid: e688136e-e06b-46ba-bec9-b8db2f9c468d

ms.date: 12/05/2018
ms.keywords: IObjectWithSite, IObjectWithSite interface [COM], IObjectWithSite interface [COM],described, _ole_iobjectwithsite, com.iobjectwithsite, ocidl/IObjectWithSite
ms.topic: interface
f1_keywords: 
 - "ocidl/IObjectWithSite"
dev_langs:
 - c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IObjectWithSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectWithSite interface


## -description


Provides a simple way to support communication between an object and its site in the container.

Often an object needs to communicate directly with a container site object and, in effect, manage the site object itself. Outside of <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a>, there is no generic means through which an object becomes aware of its site. <b>IObjectWithSite</b> provides simple objects with a simple siting mechanism (lighter than <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>) This interface should only be used when <b>IOleObject</b> is not already in use.

Through <b>IObjectWithSite</b>, a container can pass the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer of its site to the object through <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a>. Callers can also retrieve the latest site passed to <b>SetSite</b> through <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-getsite">IObjectWithSite::GetSite</a>. This latter method is included as a hooking mechanism, allowing a third party to intercept calls from the object to the site.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectWithSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-getsite">GetSite</a>
</td>
<td align="left" width="63%">
Retrieves the latest site passed using <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">SetSite</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">SetSite</a>
</td>
<td align="left" width="63%">
Enables a container to pass an object a pointer to the interface for its site.

</td>
</tr>
</table> 

