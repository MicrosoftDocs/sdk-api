---
UID: NF:objbase.CreateFileMoniker
title: CreateFileMoniker function (objbase.h)
description: Creates a file moniker based on the specified path.
helpviewer_keywords: ["CreateFileMoniker","CreateFileMoniker function [COM]","_com_CreateFileMoniker","com.createfilemoniker","objbase/CreateFileMoniker"]
old-location: com\createfilemoniker.htm
tech.root: com
ms.assetid: d9677fa0-cda0-4b63-a21f-1fd0e27c8f3f
ms.date: 12/05/2018
ms.keywords: CreateFileMoniker, CreateFileMoniker function [COM], _com_CreateFileMoniker, com.createfilemoniker, objbase/CreateFileMoniker
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
 - CreateFileMoniker
 - objbase/CreateFileMoniker
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
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CreateFileMoniker
req.apiset: ext-ms-win-com-ole32-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# CreateFileMoniker function


## -description

Creates a file moniker based on the specified path.

## -parameters

### -param lpszPathName [in]

The path on which this moniker is to be based.

This parameter can specify a relative path, a UNC path, or a drive-letter-based path. If based on a relative path, the resulting moniker must be composed onto another file moniker before it can be bound.

### -param ppmk [out]

The address of an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>* pointer variable that receives the interface pointer to the new file moniker. When successful, the function has called <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on the file moniker and the caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a>. When an error occurs, the value of the interface pointer is <b>NULL</b>.

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
The moniker was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_SYNTAX</b></dt>
</dl>
</td>
<td width="60%">
There was an error in the syntax of the path.

</td>
</tr>
</table>

## -remarks

<b>CreateFileMoniker</b> creates a moniker for an object that is stored in a file. A moniker provider (an object that provides monikers to other objects) can call this function to create a moniker to identify a file-based object that it controls, and can then make the pointer to this moniker available to other objects. An object identified by a file moniker must also implement the <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> interface so it can be loaded when a file moniker is bound.

When each object resides in its own file, as in an OLE server application that supports linking only to file-based documents in their entirety, file monikers are the only type of moniker necessary. To identify objects smaller than a file, the moniker provider must use another type of moniker (such as an item moniker) in addition to file monikers, creating a composite moniker. Composite monikers would be needed in an OLE server application that supports linking to objects smaller than a document (such as sections of a document or embedded objects).

A file moniker can be composed to the right only of another file moniker when the first moniker is based on an absolute path and the other is a relative path, resulting in a single file moniker based on the combination of the two paths. A moniker composed to the right of another moniker must be a refinement of that moniker, and the file moniker represents the largest unit of storage. To identify objects stored within a file, you would compose other types of monikers (usually item monikers) to the right of a file moniker.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
