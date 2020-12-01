---
UID: NF:rend.ITDirectoryObject.get_ObjectType
title: ITDirectoryObject::get_ObjectType (rend.h)
description: The get_ObjectType method gets a DIRECTORY_OBJECT_TYPE descriptor of the object.
helpviewer_keywords: ["ITDirectoryObject interface [TAPI 2.2]","get_ObjectType method","ITDirectoryObject.get_ObjectType","ITDirectoryObject::get_ObjectType","_tapi3_itdirectoryobject_get_objecttype","get_ObjectType","get_ObjectType method [TAPI 2.2]","get_ObjectType method [TAPI 2.2]","ITDirectoryObject interface","rend/ITDirectoryObject::get_ObjectType","tapi3.itdirectoryobject_get_objecttype"]
old-location: tapi3\itdirectoryobject_get_objecttype.htm
tech.root: tapi3
ms.assetid: b71f5286-d97d-4129-942b-fa4d4ef0943e
ms.date: 12/05/2018
ms.keywords: ITDirectoryObject interface [TAPI 2.2],get_ObjectType method, ITDirectoryObject.get_ObjectType, ITDirectoryObject::get_ObjectType, _tapi3_itdirectoryobject_get_objecttype, get_ObjectType, get_ObjectType method [TAPI 2.2], get_ObjectType method [TAPI 2.2],ITDirectoryObject interface, rend/ITDirectoryObject::get_ObjectType, tapi3.itdirectoryobject_get_objecttype
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDirectoryObject::get_ObjectType
 - rend/ITDirectoryObject::get_ObjectType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObject.get_ObjectType
---

# ITDirectoryObject::get_ObjectType


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_ObjectType</b> method gets a 
<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a> descriptor of the object.

## -parameters

### -param pObjectType [out]

Pointer to descriptor of directory object type.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rend/ne-rend-directory_object_type">DIRECTORY_OBJECT_TYPE</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>