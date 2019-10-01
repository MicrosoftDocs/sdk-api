---
UID: NN:shlobj_core.IObjMgr
title: IObjMgr (shlobj_core.h)
author: windows-sdk-content
description: Exposes methods that allow a client to append or remove an object from a collection of objects managed by a server object.
old-location: shell\IObjMgr.htm
tech.root: shell
ms.assetid: c0556a87-2be5-43dc-9ca6-dfbdae7e7137
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IObjMgr, IObjMgr interface [Windows Shell], IObjMgr interface [Windows Shell],described, _win32_IObjMgr, shell.IObjMgr, shlobj_core/IObjMgr
ms.topic: interface
f1_keywords: 
 - "shlobj_core/IObjMgr"
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IObjMgr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjMgr interface


## -description


Exposes methods that allow a client to append or remove an object from a collection of objects managed by a server object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iobjmgr-append">Append</a>
</td>
<td align="left" width="63%">
Appends an object to the collection of managed objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iobjmgr-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an object from the collection of managed objects.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by objects that manage a collection of other objects. It is exported to allow clients of the object to request that objects be added to or removed from the collection.

Use this interface to add or delete an object from the server object's collection of managed objects.



