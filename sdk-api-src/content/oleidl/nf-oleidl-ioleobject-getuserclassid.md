---
UID: NF:oleidl.IOleObject.GetUserClassID
title: IOleObject::GetUserClassID (oleidl.h)
description: Retrieves an object's class identifier, the CLSID corresponding to the string identifying the object to an end user.
helpviewer_keywords: ["GetUserClassID","GetUserClassID method [COM]","GetUserClassID method [COM]","IOleObject interface","IOleObject interface [COM]","GetUserClassID method","IOleObject.GetUserClassID","IOleObject::GetUserClassID","_ole_ioleobject_getuserclassid","com.ioleobject_getuserclassid","oleidl/IOleObject::GetUserClassID"]
old-location: com\ioleobject_getuserclassid.htm
tech.root: com
ms.assetid: 4b3c0292-0476-4f56-abd2-2f3a82195c67
ms.date: 12/05/2018
ms.keywords: GetUserClassID, GetUserClassID method [COM], GetUserClassID method [COM],IOleObject interface, IOleObject interface [COM],GetUserClassID method, IOleObject.GetUserClassID, IOleObject::GetUserClassID, _ole_ioleobject_getuserclassid, com.ioleobject_getuserclassid, oleidl/IOleObject::GetUserClassID
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
 - IOleObject::GetUserClassID
 - oleidl/IOleObject::GetUserClassID
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
 - IOleObject.GetUserClassID
---

# IOleObject::GetUserClassID


## -description

Retrieves an object's class identifier, the CLSID corresponding to the string identifying the object to an end user.

## -parameters

### -param pClsid [out]

Pointer to the class identifier (CLSID) to be returned. An object's CLSID is the binary equivalent of the user-type name returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>.

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
The operation failed.

</td>
</tr>
</table>

## -remarks

<b>IOleObject::GetUserClassID</b> returns the CLSID associated with the object in the registration database. Normally, this value is identical to the CLSID stored with the object, which is returned by <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a>. For linked objects, this is the CLSID of the last bound link source. If the object is running in an application different from the one in which it was created and for the purpose of being edited is emulating a class that the container application recognizes, the CLSID returned will be that of the class being emulated rather than that of the object's own class.

## -see-also

<a href="/windows/desktop/api/coml2api/nf-coml2api-getconvertstg">GetConvertStg</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oledoautoconvert">OleDoAutoConvert</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetautoconvert">OleSetAutoConvert</a>



<a href="/windows/desktop/api/ole2/nf-ole2-setconvertstg">SetConvertStg</a>