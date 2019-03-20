---
UID: NN:shlobj.IShellImageStore
title: IShellImageStore (shlobj.h)
author: windows-sdk-content
description: Deprecated. Exposes methods that manipulate the image cache.
old-location: shell\IShellImageStore.htm
tech.root: shell
ms.assetid: 746bd660-17b6-4669-8f23-254f5d7dde82
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellImageStore, IShellImageStore interface [Windows Shell], IShellImageStore interface [Windows Shell],described, _win32_IShellImageStore, shell.IShellImageStore, shlobj/IShellImageStore
ms.topic: interface
req.header: shlobj.h
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageStore interface


## -description


Deprecated. Exposes methods that manipulate the image cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellImageStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellImageStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellImageStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6228228a-1c12-467c-849c-b360d79ee5ca">Close</a>
</td>
<td align="left" width="63%">
Closes the image cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99ae5347-b140-4698-9fc5-bd60870d9149">Commit</a>
</td>
<td align="left" width="63%">
Writes the contents specified by <i>pdwLoc</i> to storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/580e2901-ae08-4c9f-99ee-7ba2f7fe6e52">GetEntry</a>
</td>
<td align="left" width="63%">
Gets a handle to an image in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/571df609-9d17-415c-a4e0-23c4e1523993">IsEntryInStore</a>
</td>
<td align="left" width="63%">
Checks to see if the image is in the store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2aebf791-7681-42b3-8ffe-46e103e7c036">Open</a>
</td>
<td align="left" width="63%">
Opens the storage and returns a lock.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  <b>IShellImageStore</b> is supported through Windows XP. It is not supported in later operating systems.</div>
<div> </div>


