---
UID: NN:shobjidl_core.ITaskbarList2
title: ITaskbarList2
author: windows-sdk-content
description: Extends the ITaskbarList interface by exposing a method to mark a window as a full-screen display.
old-location: shell\ITaskbarList2.htm
tech.root: shell
ms.assetid: 8af23586-349f-4d21-98cb-0aaa27a586ff
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITaskbarList2, ITaskbarList2 interface [Windows Shell], ITaskbarList2 interface [Windows Shell],described, shell.ITaskbarList2, shell_ITaskbarList2, shobjidl_core/ITaskbarList2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ITaskbarList2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a> interface by exposing a method to mark a window as a full-screen display.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskbarList2</b> interface inherits from <a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>. <b>ITaskbarList2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskbarList2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17b4a9ff-f5a2-4178-971b-f80d65d72fb5">MarkFullscreenWindow</a>
</td>
<td align="left" width="63%">
Marks a window as full-screen.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a> interface, from which it inherits.

The Shell also automatically attempts to detect full-screen applications, but it is not as reliable as using the <a href="https://msdn.microsoft.com/17b4a9ff-f5a2-4178-971b-f80d65d72fb5">ITaskbarList2::MarkFullscreenWindow</a> method. 



