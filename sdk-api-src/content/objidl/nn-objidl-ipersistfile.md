---
UID: NN:objidl.IPersistFile
title: IPersistFile (objidl.h)

description: Enables an object to be loaded from or saved to a disk file, rather than a storage object or stream.
old-location: com\ipersistfile.htm
tech.root: com
ms.assetid: 7d34507f-8a16-43b4-8225-010798abc546

ms.date: 12/05/2018
ms.keywords: IPersistFile, IPersistFile interface [COM], IPersistFile interface [COM],described, _com_ipersistfile, com.ipersistfile, objidl/IPersistFile
ms.topic: interface
f1_keywords: 
 - "objidl/IPersistFile"
dev_langs:
 - c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersistFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistFile interface


## -description


Enables an object to be loaded from or saved to a disk file, rather than a storage object or stream. Because the information needed to open a file varies greatly from one application to another, the implementation of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> on the object must also open its disk file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistFile</b> interface inherits from <b>IPersist</b>. <b>IPersistFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-getcurfile">GetCurFile</a>
</td>
<td align="left" width="63%">
Retrieves the current name of the file associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-isdirty">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">Load</a>
</td>
<td align="left" width="63%">
Opens the specified file and initializes an object from the file contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">Save</a>
</td>
<td align="left" width="63%">
Saves a copy of the object to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted">SaveCompleted</a>
</td>
<td align="left" width="63%">
Notifies the object that it can write to its file.

</td>
</tr>
</table> 

