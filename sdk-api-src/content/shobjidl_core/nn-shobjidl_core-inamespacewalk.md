---
UID: NN:shobjidl_core.INamespaceWalk
title: INamespaceWalk
author: windows-sdk-content
description: Exposes methods that walk a namespace from a given root node. The depth of the walk is specified and an optional array is returned containing the IDs of all nodes walked.
old-location: shell\INamespaceWalk.htm
tech.root: shell
ms.assetid: 164732ae-1c72-465c-a16b-a8eeaa9cc185
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: INamespaceWalk, INamespaceWalk interface [Windows Shell], INamespaceWalk interface [Windows Shell],described, _win32_INamespaceWalk, shell.INamespaceWalk, shobjidl_core/INamespaceWalk
ms.prod: windows
ms.technology: windows-sdk
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
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - INamespaceWalk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INamespaceWalk interface


## -description


Exposes methods that walk a namespace from a given root node. The depth of the walk is specified and an optional array is returned containing the IDs of all nodes walked.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamespaceWalk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INamespaceWalk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamespaceWalk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51bce109-8f84-4852-bec5-e4f2937c31b3">GetIDArrayResult</a>
</td>
<td align="left" width="63%">
Gets a list of objects found during a namespace walk initiated by <a href="https://msdn.microsoft.com/cfe328f4-6db5-423b-b944-f0f390359793">INamespaceWalk::Walk</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfe328f4-6db5-423b-b944-f0f390359793">Walk</a>
</td>
<td align="left" width="63%">
Initiates a recursive walk of the namespace from the specified root to the given depth.

</td>
</tr>
</table> 


## -remarks



Use this interface to display or perform an operation on the contents of the namespace. <b>INamespaceWalk</b> allows retrieval of all reachable nodes of your namespace as pointers to item identifier lists (PIDLs), which can in turn be used to retrieve the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> object for each.

The class identifier (CLSID) for the default implementation of <b>INamespaceWalk</b> is CLSID_NamespaceWalker. You can obtain an <b>INamespaceWalk</b> object by creating a single uninitialized object of the class associated with CLSID_NamespaceWalker using <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>. This interface's IID is IID_INamespaceWalk.




## -see-also




<a href="https://msdn.microsoft.com/15244d6e-6cd7-4dee-8e4e-2533d5a60ae7">INamespaceWalkCB</a>
 

 

