---
UID: NF:ole2.OleRegEnumFormatEtc
title: OleRegEnumFormatEtc function (ole2.h)
description: Creates an enumeration object that can be used to enumerate data formats that an OLE object server has registered in the system registry.
helpviewer_keywords: ["OleRegEnumFormatEtc","OleRegEnumFormatEtc function [COM]","_ole_OleRegEnumFormatEtc","com.oleregenumformatetc","ole2/OleRegEnumFormatEtc"]
old-location: com\oleregenumformatetc.htm
tech.root: com
ms.assetid: 6caebc68-a136-40f2-92d8-7f8003c18e5c
ms.date: 12/05/2018
ms.keywords: OleRegEnumFormatEtc, OleRegEnumFormatEtc function [COM], _ole_OleRegEnumFormatEtc, com.oleregenumformatetc, ole2/OleRegEnumFormatEtc
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
 - OleRegEnumFormatEtc
 - ole2/OleRegEnumFormatEtc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleRegEnumFormatEtc
---

# OleRegEnumFormatEtc function


## -description

Creates an enumeration object that can be used to enumerate data formats that an OLE object server has registered in the system registry. An object application or object handler calls this function when it must enumerate those formats. Developers of custom DLL object applications use this function to emulate the behavior of the default object handler.

## -parameters

### -param clsid [in]

CLSID of the class whose formats are being requested.

### -param dwDirection [in]

Indicates whether to enumerate formats that can be passed to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> or formats that can be passed to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>. Possible values are taken from the enumeration <a href="/windows/desktop/api/objidl/ne-objidl-datadir">DATADIR</a>.

### -param ppenum [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> pointer variable that receives the interface pointer to the enumeration object.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
There is no CLSID registered for the class object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB</b></dt>
</dl>
</td>
<td width="60%">
There was an error reading the registry.

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

Object applications can ask OLE to create an enumeration object for <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures to enumerate supported data formats in one of two ways. One way is to call <b>OleRegEnumFormatEtc</b>. The other is to return OLE_S_USEREG in response to calls by the default object handler to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumformatetc">IDataObject::EnumFormatEtc</a>. OLE_S_USEREG instructs the default handler to call <b>OleRegEnumFormatEtc</b>. Because DLL object applications cannot return OLE_S_USEREG, they must call <b>OleRegEnumFormatEtc</b> rather than delegating the job to the object handler. With the supplied <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> pointer to the object, you can call the standard enumeration object methods to do the enumeration.



The <b>OleRegEnumFormatEtc</b> function and its sibling functions, <a href="/windows/desktop/api/ole2/nf-ole2-olereggetusertype">OleRegGetUserType</a>, <a href="/windows/desktop/api/ole2/nf-ole2-olereggetmiscstatus">OleRegGetMiscStatus</a>, and <a href="/windows/desktop/api/ole2/nf-ole2-oleregenumverbs">OleRegEnumVerbs</a>, provide a way for developers of custom DLL object applications to emulate the behavior of OLE's default object handler in getting information about objects from the registry. By using these functions, you avoid the considerable work of writing your own, and the pitfalls inherent in working directly in the registry. In addition, you get future enhancements and optimizations of these functions without having to code them yourself.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-enumformatetc">IDataObject::EnumFormatEtc</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>