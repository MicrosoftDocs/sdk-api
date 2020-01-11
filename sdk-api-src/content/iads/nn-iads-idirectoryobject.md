---
UID: NN:iads.IDirectoryObject
title: IDirectoryObject (iads.h)
description: The IDirectoryObject interface is a non-Automation COM interface that provides clients with direct access to directory service objects.
old-location: adsi\idirectoryobject.htm
tech.root: adsi
ms.assetid: bc4f8920-2881-4393-bb01-ed837c3db6ad
ms.date: 12/05/2018
ms.keywords: IDirectoryObject, IDirectoryObject interface [ADSI], IDirectoryObject interface [ADSI],described, _ds_idirectoryobject_ref, adsi.idirectoryobject, adsi.idirectoryobject__ref, iads/IDirectoryObject
f1_keywords:
- iads/IDirectoryObject
dev_langs:
- c++
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Activeds.dll
api_name:
- IDirectoryObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectoryObject interface


## -description


The <b>IDirectoryObject</b> interface is a non-Automation COM interface that provides clients with direct access to directory service objects. The interface enables access by means of a direct over-the-wire protocol, rather than through the ADSI attribute cache. Using the over-the-wire protocol optimizes performance. With <b>IDirectoryObject</b>, a client can get, or set, any number of object attributes with one method call. Unlike the corresponding Automation methods, which are invoked in batch, those of <b>IDirectoryObject</b> are executed when they are called. <b>IDirectoryObject</b> performs no attribute caching.
   

Non-Automation clients can call the methods of <b>IDirectoryObject</b> to optimize performance and take advantage of native directory service interfaces. Automation clients cannot use <b>IDirectoryObject</b>. Instead, they should use the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a> interface.

Of the ADSI system-supplied providers, only the LDAP provider supports this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectoryObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectoryObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectoryObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject">CreateDSObject</a>
</td>
<td align="left" width="63%">
Creates a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-idirectoryobject-deletedsobject">DeleteDSObject</a>
</td>
<td align="left" width="63%">
Deletes a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes">GetObjectAttributes</a>
</td>
<td align="left" width="63%">
Gets one or more attributes of a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectinformation">GetObjectInformation</a>
</td>
<td align="left" width="63%">
Gets data about a directory service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes">SetObjectAttributes</a>
</td>
<td align="left" width="63%">
Sets one or more attributes of a directory service object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iads">IADs</a>
 

 

