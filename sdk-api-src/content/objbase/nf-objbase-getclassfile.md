---
UID: NF:objbase.GetClassFile
title: GetClassFile function (objbase.h)
description: Returns the CLSID associated with the specified file name.
helpviewer_keywords: ["GetClassFile","GetClassFile function [COM]","_com_GetClassFile","com.getclassfile","objbase/GetClassFile"]
old-location: com\getclassfile.htm
tech.root: com
ms.assetid: dc3cb263-7b9a-45f9-8eab-3a88aa9392db
ms.date: 12/05/2018
ms.keywords: GetClassFile, GetClassFile function [COM], _com_GetClassFile, com.getclassfile, objbase/GetClassFile
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetClassFile
 - objbase/GetClassFile
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
 - Ole32.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
api_name:
 - GetClassFile
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# GetClassFile function


## -description

Returns the CLSID associated with the specified file name.

## -parameters

### -param szFilename [in]

A pointer to the filename for which you are requesting the associated CLSID.

### -param pclsid [out]

A pointer to the location where the associated CLSID is written on return.

## -returns

This function can return any of the file system errors, as well as the following values.

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
The CLSID was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_CANTOPENFILE</b></dt>
</dl>
</td>
<td width="60%">
Unable to open the specified file name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_INVALIDEXTENSION</b></dt>
</dl>
</td>
<td width="60%">
The specified extension in the registry is invalid.

</td>
</tr>
</table>

## -remarks

When given a file name, <b>GetClassFile</b> finds the CLSID associated with that file. Examples of its use are in the <a href="/windows/desktop/api/ole/nf-ole-olecreatefromfile">OleCreateFromFile</a> function, which is passed a file name and requires an associated CLSID, and in the OLE implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a>, which, when a link to a file-based document is activated, calls <b>GetClassFile</b> to locate the object application that can open the file. 



<b>GetClassFile</b> uses the following strategies to determine an appropriate CLSID: 

<ol>
<li>
If the file contains a storage object, as determined by a call to the <a href="/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile">StgIsStorageFile</a> function, <b>GetClassFile</b> returns the CLSID that was written with the <a href="/windows/desktop/api/objidl/nf-objidl-istorage-setclass">IStorage::SetClass</a> method.

</li>
<li>
If the file is not a storage object, <b>GetClassFile</b> attempts to match various bits in the file against a pattern in the registry. A pattern in the registry can contain a series of entries of the form:

entry = <i>offset</i>, <i>cb</i>, <i>mask</i>, <i>value</i>

The value of the <i>offset</i> item is an offset from the beginning or end of the file and the <i>cb</i> item is a length in bytes. These two values represent a particular byte range in the file. (A negative value for the offset item is interpreted from the end of the file). The <i>mask</i> value is a bitmask that is used to perform a logical AND operation with the byte range specified by <i>offset</i> and <i>cb</i>. The result of the logical AND operation is compared with the <i>value</i> item. If the <i>mask</i> is omitted, it is assumed to be all ones.

Each pattern in the registry is compared to the file in the order of the patterns in the database. The first pattern where each of the value items matches the result of the AND operation determines the CLSID of the file. For example, the pattern contained in the following entries of the registry requires that the first four bytes be AB CD 12 34 and that the last four bytes be FE FE FE FE:

<pre><b>HKEY_CLASSES_ROOT </b>
   <b>FileType</b>
      <b>{12345678-0000-0001-C000-000000000095}</b>
         <b>0</b> = 0, 4, FFFFFFFF, ABCD1234 
         <b>1</b> = -4, 4, , FEFEFEFE </pre>
If a file contains such a pattern, the CLSID {12345678-0000-0001-C000-000000000095} will be associated with this file.

</li>
<li>
If the above strategies fail, <b>GetClassFile</b> searches for the <b>File Extension</b> key in the registry that corresponds to the .ext portion of the file name. If the database entry contains a valid CLSID, <b>GetClassFile</b> returns that CLSID.

</li>
<li>
If all strategies fail, the function returns MK_E_INVALIDEXTENSION.

</li>
</ol>

## -see-also

<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a>
