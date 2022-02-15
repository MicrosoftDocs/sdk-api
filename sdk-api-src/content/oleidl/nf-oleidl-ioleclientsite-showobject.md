---
UID: NF:oleidl.IOleClientSite.ShowObject
title: IOleClientSite::ShowObject (oleidl.h)
description: Asks a container to display its object to the user. This method ensures that the container itself is visible and not minimized.
helpviewer_keywords: ["IOleClientSite interface [COM]","ShowObject method","IOleClientSite.ShowObject","IOleClientSite::ShowObject","ShowObject","ShowObject method [COM]","ShowObject method [COM]","IOleClientSite interface","_ole_ioleclientsite_showobject","com.ioleclientsite_showobject","oleidl/IOleClientSite::ShowObject"]
old-location: com\ioleclientsite_showobject.htm
tech.root: com
ms.assetid: ba502a3d-2042-4978-a152-636a887c61fc
ms.date: 12/05/2018
ms.keywords: IOleClientSite interface [COM],ShowObject method, IOleClientSite.ShowObject, IOleClientSite::ShowObject, ShowObject, ShowObject method [COM], ShowObject method [COM],IOleClientSite interface, _ole_ioleclientsite_showobject, com.ioleclientsite_showobject, oleidl/IOleClientSite::ShowObject
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
 - IOleClientSite::ShowObject
 - oleidl/IOleClientSite::ShowObject
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
 - IOleClientSite.ShowObject
---

# IOleClientSite::ShowObject


## -description

Asks a container to display its object to the user. This method ensures that the container itself is visible and not minimized.



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
<dt><b>OLE_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Client site is in an OLE 1 container.

</td>
</tr>
</table>

## -remarks

After a link client binds to a link source, it commonly calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a> on the link source, usually requesting the source to perform some action requiring that it display itself to the user. As part of its implementation of <b>IOleObject::DoVerb</b>, the link source can call <b>ShowObject</b>, which forces the client to show the link source as best it can. If the link source's container is itself an embedded object, it will recursively invoke <b>ShowObject</b> on its own container.

Having called the <b>ShowObject</b> method, a link source has no guarantee of being appropriately displayed because its container may not be able to do so at the time of the call. The <b>ShowObject</b> method does not guarantee visibility, only that the container will do the best it can.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a>
