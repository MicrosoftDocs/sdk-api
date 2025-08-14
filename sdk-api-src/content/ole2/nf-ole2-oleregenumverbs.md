---
UID: NF:ole2.OleRegEnumVerbs
title: OleRegEnumVerbs function (ole2.h)
description: Supplies an enumeration of the registered verbs for the specified class. Developers of custom DLL object applications use this function to emulate the behavior of the default object handler.
helpviewer_keywords: ["OleRegEnumVerbs","OleRegEnumVerbs function [COM]","_ole_OleRegEnumVerbs","com.oleregenumverbs","ole2/OleRegEnumVerbs"]
old-location: com\oleregenumverbs.htm
tech.root: com
ms.assetid: 25cd0876-90b6-4fa3-b180-ffa0c3b51497
ms.date: 12/05/2018
ms.keywords: OleRegEnumVerbs, OleRegEnumVerbs function [COM], _ole_OleRegEnumVerbs, com.oleregenumverbs, ole2/OleRegEnumVerbs
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
 - OleRegEnumVerbs
 - ole2/OleRegEnumVerbs
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
 - OleRegEnumVerbs
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleRegEnumVerbs function


## -description

Supplies an enumeration of the registered verbs for the specified class. Developers of custom DLL object applications use this function to emulate the behavior of the default object handler.

## -parameters

### -param clsid [in]

Class identifier whose verbs are being requested.

### -param ppenum [out]

Address of <a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>* pointer variable that receives the interface pointer to the new enumeration object.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEOBJ_E_NOVERBS</b></dt>
</dl>
</td>
<td width="60%">
No verbs are registered for the class.

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
An error occurred reading the registry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_REGDB_KEY</b></dt>
</dl>
</td>
<td width="60%">
The DataFormats/GetSet key is missing from the registry.


</td>
</tr>
</table>

## -remarks

Object applications can ask OLE to create an enumeration object for <a href="/windows/desktop/api/oleidl/ns-oleidl-oleverb">OLEVERB</a> structures to enumerate supported verbs in one of two ways. One way is to call <b>OleRegEnumVerbs</b>. The other way is to return OLE_S_USEREG in response to calls by the default object handler to <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>. OLE_S_USEREG instructs the default handler to call <b>OleRegEnumVerbs</b>. Because DLL object applications cannot return OLE_S_USEREG, they must call <b>OleRegEnumVerbs</b> rather than delegating the job to the object handler. With the supplied <a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a> pointer to the object, you can call the standard enumeration object methods to do the enumeration.

The <b>OleRegEnumVerbs</b> function and its sibling functions, <a href="/windows/desktop/api/ole2/nf-ole2-olereggetusertype">OleRegGetUserType</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olereggetmiscstatus">OleRegGetMiscStatus</a>, and <a href="/windows/desktop/api/ole2/nf-ole2-oleregenumformatetc">OleRegEnumFormatEtc</a>, provide a way for developers of custom DLL object applications to emulate the behavior of OLE's default object handler in getting information about objects from the registry. By using these functions, you avoid the considerable work of writing your own, and the pitfalls inherent in working directly in the registry. In addition, you get future enhancements and optimizations of these functions without having to code them yourself.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumverbs">IOleObject::EnumVerbs</a>
