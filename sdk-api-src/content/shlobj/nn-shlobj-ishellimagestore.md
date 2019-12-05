---
UID: NN:shlobj.IShellImageStore
title: IShellImageStore (shlobj.h)
description: Deprecated. Exposes methods that manipulate the image cache.
old-location: shell\IShellImageStore.htm
tech.root: shell
ms.assetid: 746bd660-17b6-4669-8f23-254f5d7dde82
ms.date: 12/05/2018
ms.keywords: IShellImageStore, IShellImageStore interface [Windows Shell], IShellImageStore interface [Windows Shell],described, _win32_IShellImageStore, shell.IShellImageStore, shlobj/IShellImageStore
ms.topic: interface
f1_keywords:
- shlobj/IShellImageStore
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellImageStore interface


## -description


Deprecated. Exposes methods that manipulate the image cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellImageStore</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellImageStore</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellimagestore-close">Close</a>
</td>
<td align="left" width="63%">
Closes the image cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellimagestore-commit">Commit</a>
</td>
<td align="left" width="63%">
Writes the contents specified by <i>pdwLoc</i> to storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellimagestore-getentry">GetEntry</a>
</td>
<td align="left" width="63%">
Gets a handle to an image in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellimagestore-isentryinstore">IsEntryInStore</a>
</td>
<td align="left" width="63%">
Checks to see if the image is in the store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj/nf-shlobj-ishellimagestore-open">Open</a>
</td>
<td align="left" width="63%">
Opens the storage and returns a lock.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  <b>IShellImageStore</b> is supported through Windows XP. It is not supported in later operating systems.</div>
<div> </div>


