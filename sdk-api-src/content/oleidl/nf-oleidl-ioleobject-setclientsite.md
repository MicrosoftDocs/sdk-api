---
UID: NF:oleidl.IOleObject.SetClientSite
title: IOleObject::SetClientSite (oleidl.h)
description: Informs an embedded object of its display location, called a &quot;client site,&quot; within its container.
helpviewer_keywords: ["IOleObject interface [COM]","SetClientSite method","IOleObject.SetClientSite","IOleObject::SetClientSite","SetClientSite","SetClientSite method [COM]","SetClientSite method [COM]","IOleObject interface","_ole_ioleobject_setclientsite","com.ioleobject_setclientsite","oleidl/IOleObject::SetClientSite"]
old-location: com\ioleobject_setclientsite.htm
tech.root: com
ms.assetid: 6690b5a3-bada-496c-89cb-a9ae1fc9dfb0
ms.date: 12/05/2018
ms.keywords: IOleObject interface [COM],SetClientSite method, IOleObject.SetClientSite, IOleObject::SetClientSite, SetClientSite, SetClientSite method [COM], SetClientSite method [COM],IOleObject interface, _ole_ioleobject_setclientsite, com.ioleobject_setclientsite, oleidl/IOleObject::SetClientSite
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleObject::SetClientSite
 - oleidl/IOleObject::SetClientSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.SetClientSite
---

# IOleObject::SetClientSite


## -description

Informs an embedded object of its display location, called a "client site," within its container.

## -parameters

### -param pClientSite [in]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> interface on the container application's client-site.

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

Within a compound document, each embedded object has its own client site - the place where it is displayed and through which it receives information about its storage, user interface, and other resources. <b>IOleObject::SetClientSite</b> is the only method enabling an embedded object to obtain a pointer to its client site.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A container can notify an object of its client site either at the time the object is created or, subsequently, when the object is initialized.

When creating or loading an object, a container may pass a client-site pointer (along with other arguments) to one of the following helper functions: <a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>, <a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>. These helper functions load an object handler for the new object and call <b>IOleObject::SetClientSite</b> on the container's behalf before returning a pointer to the new object.

Passing a client-site pointer informs the object handler that the client site is ready to process requests. If the client site is unlikely to be ready immediately after the handler is loaded, you may want your container to pass a <b>NULL</b> client-site pointer to the helper function. The <b>NULL</b> pointer says that no client site is available and thereby defers notifying the object handler of the client site until the object is initialized. In response, the helper function returns a pointer to the object, but upon receiving that pointer the container must call <b>IOleObject::SetClientSite</b> as part of initializing the new object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementation consists simply of incrementing the reference count on, and storing, the pointer to the client site.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getclientsite">IOleObject::GetClientSite</a>



<a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>



<a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>