---
UID: NN:objidl.IPersistFile
title: IPersistFile (objidl.h)
author: windows-sdk-content
description: Enables an object to be loaded from or saved to a disk file, rather than a storage object or stream.
old-location: com\ipersistfile.htm
tech.root: com
ms.assetid: 7d34507f-8a16-43b4-8225-010798abc546
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersistFile, IPersistFile interface [COM], IPersistFile interface [COM],described, _com_ipersistfile, com.ipersistfile, objidl/IPersistFile
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistFile interface


## -description


Enables an object to be loaded from or saved to a disk file, rather than a storage object or stream. Because the information needed to open a file varies greatly from one application to another, the implementation of <a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">IPersistFile::Load</a> on the object must also open its disk file.


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
<a href="https://msdn.microsoft.com/61f1751d-47ce-4b3f-9876-24ddd542dacb">GetCurFile</a>
</td>
<td align="left" width="63%">
Retrieves the current name of the file associated with the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f3df841-d7fe-472e-a13c-124fdf425a35">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an object has changed since it was last saved to its current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8391aa5c-fe6e-4b03-9eef-7958f75910a5">Load</a>
</td>
<td align="left" width="63%">
Opens the specified file and initializes an object from the file contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da9581e8-98c7-4592-8ee1-a1bc8232635b">Save</a>
</td>
<td align="left" width="63%">
Saves a copy of the object to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eda29981-0c24-409a-8fb9-2dc2eb96d108">SaveCompleted</a>
</td>
<td align="left" width="63%">
Notifies the object that it can write to its file.

</td>
</tr>
</table> 

