---
UID: NF:ole2.OleRegGetUserType
title: OleRegGetUserType function (ole2.h)
description: Gets the user type of the specified class from the registry.
helpviewer_keywords: ["OleRegGetUserType","OleRegGetUserType function [COM]","_com_OleRegGetUserType","com.olereggetusertype","ole2/OleRegGetUserType"]
old-location: com\olereggetusertype.htm
tech.root: com
ms.assetid: 492a4084-494e-4d78-8f3a-853ec486a2d6
ms.date: 12/05/2018
ms.keywords: OleRegGetUserType, OleRegGetUserType function [COM], _com_OleRegGetUserType, com.olereggetusertype, ole2/OleRegGetUserType
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleRegGetUserType
 - ole2/OleRegGetUserType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleRegGetUserType
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleRegGetUserType function


## -description

Gets the user type of the specified class from the registry. 

Developers of custom DLL object applications use this function to emulate the behavior of the OLE default handler.

## -parameters

### -param clsid [in]

The CLSID of the class for which the user type is to be requested.

### -param dwFormOfType [in]

The form of the user-presentable string. Possible values are taken from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-userclasstype">USERCLASSTYPE</a>.

### -param pszUserType [out]

A pointer to a string that receives the user type.

## -returns

This function can return the standard return value E_OUTOFMEMORY, as well as the following values.

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
The user type was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
No CLSID is registered for the class object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
There was an error reading from the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_REGDB_KEY</b></dt>
</dl>
</td>
<td width="60%">
The  <b>ProgID</b> = <i>MainUserTypeName</i> and <b>CLSID</b> = <i>MainUserTypeName</i> keys  are missing from the registry.


</td>
</tr>
</table>

## -remarks

Object applications can ask OLE to get the user type name of a specified class in one of two ways. One way is to call <b>OleRegGetUserType</b>. The other is to return OLE_S_USEREG in response to calls by the default object handler to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>. OLE_S_USEREG instructs the default handler to call <b>OleRegGetUserType</b>. Because DLL object applications cannot return OLE_S_USEREG, they must call <b>OleRegGetUserType</b>, rather than delegating the job to the object handler.



The <b>OleRegGetUserType</b> function and its sibling functions, <a href="/windows/desktop/api/ole2/nf-ole2-olereggetmiscstatus">OleRegGetMiscStatus</a>, <a href="/windows/desktop/api/ole2/nf-ole2-oleregenumformatetc">OleRegEnumFormatEtc</a>, and <a href="/windows/desktop/api/ole2/nf-ole2-oleregenumverbs">OleRegEnumVerbs</a>, provide a way for developers of custom DLL object applications to emulate the behavior of OLE's default object handler in getting information about objects from the registry. By using these functions, you avoid the considerable work of writing your own, and the pitfalls inherent in working directly in the registry. In addition, you get future enhancements and optimizations of these functions without having to code them yourself.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getusertype">IOleObject::GetUserType</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleregenumformatetc">OleRegEnumFormatEtc</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleregenumverbs">OleRegEnumVerbs</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olereggetmiscstatus">OleRegGetMiscStatus</a>
