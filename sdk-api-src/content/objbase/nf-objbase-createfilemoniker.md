---
UID: NF:objbase.CreateFileMoniker
title: CreateFileMoniker function
author: windows-sdk-content
description: Creates a file moniker based on the specified path.
old-location: com\createfilemoniker.htm
old-project: com
ms.assetid: d9677fa0-cda0-4b63-a21f-1fd0e27c8f3f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateFileMoniker, CreateFileMoniker function [COM], _com_CreateFileMoniker, com.createfilemoniker, objbase/CreateFileMoniker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CreateFileMoniker
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# CreateFileMoniker function


## -description


Creates a file moniker based on the specified path.


## -parameters




### -param lpszPathName [in]

The path on which this moniker is to be based.

This parameter can specify a relative path, a UNC path, or a drive-letter-based path. If based on a relative path, the resulting moniker must be composed onto another file moniker before it can be bound.


### -param ppmk [out]

The address of an <a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>* pointer variable that receives the interface pointer to the new file moniker. When successful, the function has called <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the file moniker and the caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. When an error occurs, the value of the interface pointer is <b>NULL</b>.


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



<b>CreateFileMoniker</b> creates a moniker for an object that is stored in a file. A moniker provider (an object that provides monikers to other objects) can call this function to create a moniker to identify a file-based object that it controls, and can then make the pointer to this moniker available to other objects. An object identified by a file moniker must also implement the <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a> interface so it can be loaded when a file moniker is bound.

When each object resides in its own file, as in an OLE server application that supports linking only to file-based documents in their entirety, file monikers are the only type of moniker necessary. To identify objects smaller than a file, the moniker provider must use another type of moniker (such as an item moniker) in addition to file monikers, creating a composite moniker. Composite monikers would be needed in an OLE server application that supports linking to objects smaller than a document (such as sections of a document or embedded objects).

A file moniker can be composed to the right only of another file moniker when the first moniker is based on an absolute path and the other is a relative path, resulting in a single file moniker based on the combination of the two paths. A moniker composed to the right of another moniker must be a refinement of that moniker, and the file moniker represents the largest unit of storage. To identify objects stored within a file, you would compose other types of monikers (usually item monikers) to the right of a file moniker.




## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

