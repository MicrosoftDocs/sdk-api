---
UID: NF:oleidl.IOleClientSite.GetContainer
title: IOleClientSite::GetContainer (oleidl.h)
description: Retrieves a pointer to the object's container.
helpviewer_keywords: ["GetContainer","GetContainer method [COM]","GetContainer method [COM]","IOleClientSite interface","IOleClientSite interface [COM]","GetContainer method","IOleClientSite.GetContainer","IOleClientSite::GetContainer","_ole_ioleclientsite_getcontainer","com.ioleclientsite_getcontainer","oleidl/IOleClientSite::GetContainer"]
old-location: com\ioleclientsite_getcontainer.htm
tech.root: com
ms.assetid: 8f0caf07-f059-4e0c-9c28-c7ad0cc149e3
ms.date: 12/05/2018
ms.keywords: GetContainer, GetContainer method [COM], GetContainer method [COM],IOleClientSite interface, IOleClientSite interface [COM],GetContainer method, IOleClientSite.GetContainer, IOleClientSite::GetContainer, _ole_ioleclientsite_getcontainer, com.ioleclientsite_getcontainer, oleidl/IOleClientSite::GetContainer
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
 - IOleClientSite::GetContainer
 - oleidl/IOleClientSite::GetContainer
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
 - IOleClientSite.GetContainer
---

# IOleClientSite::GetContainer


## -description

Retrieves a pointer to the object's container.

## -parameters

### -param ppContainer [out]

Address of <a href="/windows/desktop/api/oleidl/nn-oleidl-iolecontainer">IOleContainer</a> pointer variable that receives the interface pointer to the container object. If an error occurs, the implementation must set <i>ppContainer</i> to <b>NULL</b>.

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
The client site is in an OLE 1 container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The container does not implement the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolecontainer">IOleContainer</a> interface.

</td>
</tr>
</table>

## -remarks

If a container supports links to its embedded objects, implementing <b>GetContainer</b> enables link clients to enumerate the container's objects and recursively traverse a containment hierarchy. This method is optional but recommended for all containers that expect to support links to their embedded objects.

Link clients can traverse a hierarchy of compound-document objects by recursively calling <b>GetContainer</b> to get a pointer to the link source's container; followed by <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to get a pointer to the container's <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> interface and, finally, <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getclientsite">IOleObject::GetClientSite</a> to get the container's client site in its container.

Simple containers that do not support links to their embedded objects probably do not need to implement this method. Instead, they can return E_NOINTERFACE and set <i>ppContainer</i> to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>