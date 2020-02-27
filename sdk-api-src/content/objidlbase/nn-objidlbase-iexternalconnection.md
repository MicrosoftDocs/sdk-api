---
UID: NN:objidlbase.IExternalConnection
title: IExternalConnection (objidlbase.h)
description: Manages a server object's count of marshaled, or external, connections. A server that maintains such a count can detect when it has no external connections and shut itself down in an orderly fashion.
old-location: com\iexternalconnection.htm
tech.root: com
ms.assetid: 28afc305-d5b0-4ac9-9412-5876e575c2c2
ms.date: 12/05/2018
ms.keywords: IExternalConnection, IExternalConnection interface [COM], IExternalConnection interface [COM],described, _com_iexternalconnection, com.iexternalconnection, objidlbase/IExternalConnection
f1_keywords:
- objidlbase/IExternalConnection
dev_langs:
- c++
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
- objidlbase.h
api_name:
- IExternalConnection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExternalConnection interface


## -description


Manages a server object's count of marshaled, or external, connections. A server that maintains such a count can detect when it has no external connections and shut itself down in an orderly fashion. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExternalConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExternalConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExternalConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iexternalconnection-addconnection">AddConnection</a>
</td>
<td align="left" width="63%">
Increments the count of an object's strong external connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iexternalconnection-releaseconnection">ReleaseConnection</a>
</td>
<td align="left" width="63%">
Decrements the count of an object's strong external connections.

</td>
</tr>
</table> 


## -remarks



<b>IExternalConnection</b> is most commonly implemented on server objects, to enable the orderly shutdown of a link to an embedded object following a silent update. Objects that do not implement <b>IExternalConnection</b> risk losing data in such a situation: When the final link client releases the embedded (server) object, the last external connection on the object's stub manager is released, causing the stub manager to release its pointers to interfaces on the embedded object and initiate shutdown of the object. At this point, the server object calls <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-saveobject">IOleClientSite::SaveObject</a> on the link container, and the link container's return call to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> fails because the stub manager no longer has a pointer to the embedded object. Any unsaved changes to the server object's data would then be lost. 



If the server object implements <b>IExternalConnection</b>, however, its stub manager will not release its connection to the object when the last external connection is released. Instead, it will stay connected until the object is ready to destroy itself. 

In standard marshaling, to increment the object's count of external connections, COM calls <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iexternalconnection-addconnection">IExternalConnection::AddConnection</a> on the object when the object is first marshaled. The stub manager calls the methods of <b>IExternalConnection</b> on the object as subsequent external connections are obtained and released. When the object's count of external connections goes to zero, the object can save its data and then revoke itself from the running object table and do whatever else is necessary to reduce its object reference count to zero.

An object that implements <b>IExternalConnection</b> should explicitly call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-codisconnectobject">CoDisconnectObject</a> on itself when its external reference count drops to 0. This call will cause the stub manager to call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the object so that the object can destroy itself.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-codisconnectobject">CoDisconnectObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-colockobjectexternal">CoLockObjectExternal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>
 

 

