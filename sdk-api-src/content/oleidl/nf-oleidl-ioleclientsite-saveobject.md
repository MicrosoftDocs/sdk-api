---
UID: NF:oleidl.IOleClientSite.SaveObject
title: IOleClientSite::SaveObject (oleidl.h)
description: Saves the embedded object associated with the client site. This function is synchronous; by the time it returns, the save will be completed.
helpviewer_keywords: ["IOleClientSite interface [COM]","SaveObject method","IOleClientSite.SaveObject","IOleClientSite::SaveObject","SaveObject","SaveObject method [COM]","SaveObject method [COM]","IOleClientSite interface","_ole_ioleclientsite_saveobject","com.ioleclientsite_saveobject","oleidl/IOleClientSite::SaveObject"]
old-location: com\ioleclientsite_saveobject.htm
tech.root: com
ms.assetid: ef1a0085-f4fa-4d77-adab-0386f354dfe7
ms.date: 12/05/2018
ms.keywords: IOleClientSite interface [COM],SaveObject method, IOleClientSite.SaveObject, IOleClientSite::SaveObject, SaveObject, SaveObject method [COM], SaveObject method [COM],IOleClientSite interface, _ole_ioleclientsite_saveobject, com.ioleclientsite_saveobject, oleidl/IOleClientSite::SaveObject
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
 - IOleClientSite::SaveObject
 - oleidl/IOleClientSite::SaveObject
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
 - IOleClientSite.SaveObject
---

# IOleClientSite::SaveObject


## -description

Saves the embedded object associated with the client site. This function is synchronous; by the time it returns, the save will be completed.



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation has failed.

</td>
</tr>
</table>

## -remarks

An embedded object calls <b>SaveObject</b> to ask its container to save it to persistent storage when an end user chooses the File Update or Exit commands. The call is synchronous, meaning that by the time it returns, the save operation will be completed.

Calls to <b>SaveObject</b> occur in most implementations of <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>. Normally, when a container tells an object to close, the container passes a flag specifying whether the object should save itself before closing, prompt the user for instructions, or close without saving itself. If an object is instructed to save itself, either by its container or an end user, it calls <b>SaveObject</b> to ask the container application to save the object's contents before the object closes itself. If a container instructs an object not to save itself, the object should not call <b>SaveObject</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>
