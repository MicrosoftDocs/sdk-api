---
UID: NF:oleidl.IOleObject.GetMiscStatus
title: IOleObject::GetMiscStatus (oleidl.h)
description: Retrieves the status of an object at creation and loading.
helpviewer_keywords: ["GetMiscStatus","GetMiscStatus method [COM]","GetMiscStatus method [COM]","IOleObject interface","IOleObject interface [COM]","GetMiscStatus method","IOleObject.GetMiscStatus","IOleObject::GetMiscStatus","_ole_ioleobject_getmiscstatus","com.ioleobject_getmiscstatus","oleidl/IOleObject::GetMiscStatus"]
old-location: com\ioleobject_getmiscstatus.htm
tech.root: com
ms.assetid: 0c5e9f73-8eec-48e0-a172-4d3d49e56071
ms.date: 12/05/2018
ms.keywords: GetMiscStatus, GetMiscStatus method [COM], GetMiscStatus method [COM],IOleObject interface, IOleObject interface [COM],GetMiscStatus method, IOleObject.GetMiscStatus, IOleObject::GetMiscStatus, _ole_ioleobject_getmiscstatus, com.ioleobject_getmiscstatus, oleidl/IOleObject::GetMiscStatus
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
 - IOleObject::GetMiscStatus
 - oleidl/IOleObject::GetMiscStatus
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
 - IOleObject.GetMiscStatus
---

# IOleObject::GetMiscStatus


## -description

Retrieves the status of an object at creation and loading.

## -parameters

### -param dwAspect [in]

The aspect of an object about which status information is being requested. The value is obtained from the enumeration <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>.

### -param pdwStatus [out]

Pointer to where the status information is returned. This parameter cannot be <b>NULL</b>.

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
<dt><b>OLE_S_USEREG</b></dt>
</dl>
</td>
<td width="60%">
Delegate the retrieval of miscellaneous status information to the default handler's implementation of this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
There is no CLSID registered for the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
Error accessing the registry.

</td>
</tr>
</table>

## -remarks

A container normally calls <b>IOleObject::GetMiscStatus</b> when it creates or loads an object in order to determine how to display the object and what types of behaviors it supports.

Objects store status information in the registry. If the object is not running, the default handler's implementation of <b>IOleObject::GetMiscStatus</b> retrieves this information from the registry. If the object is running, the default handler invokes <b>IOleObject::GetMiscStatus</b> on the object itself.

The information that is actually stored in the registry varies with individual objects. The status values to be returned are defined in the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olemisc">OLEMISC</a>.

The default value of <b>IOleObject::GetMiscStatus</b> is used if a subkey corresponding to the specified <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> is not found. To set an OLE control, specify DVASPECT==1. This will cause the following to occur in the registry: 


<pre><b>HKEY_CLASSES_ROOT\CLSID\ . . .</b>
   <b>MiscStatus</b> = 1</pre>


<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementation normally consists of delegating the call to the default handler.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-olemisc">OLEMISC</a>
