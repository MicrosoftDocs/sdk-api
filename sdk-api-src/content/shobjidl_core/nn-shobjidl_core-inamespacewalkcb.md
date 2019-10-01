---
UID: NN:shobjidl_core.INamespaceWalkCB
title: INamespaceWalkCB (shobjidl_core.h)
author: windows-sdk-content
description: A callback interface exposing methods used with INamespaceWalk.
old-location: shell\INamespaceWalkCB.htm
tech.root: shell
ms.assetid: 15244d6e-6cd7-4dee-8e4e-2533d5a60ae7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INamespaceWalkCB, INamespaceWalkCB interface [Windows Shell], INamespaceWalkCB interface [Windows Shell],described, _win32_INamespaceWalkCB, shell.INamespaceWalkCB, shobjidl_core/INamespaceWalkCB
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/INamespaceWalkCB"
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
 - INamespaceWalkCB
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INamespaceWalkCB interface


## -description


A callback interface exposing methods used with <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk">INamespaceWalk</a>. After performing a walk with <b>INamespaceWalk</b>, an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object representing the walked nodes is passed to the <b>INamespaceWalkCB</b> methods. What those methods do with the information depends on the object that is implementing them.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamespaceWalkCB</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INamespaceWalkCB</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamespaceWalkCB</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-enterfolder">EnterFolder</a>
</td>
<td align="left" width="63%">
Called when a folder is about to be entered during a namespace walk. Use this method for any initialization of the retrieved item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-founditem">FoundItem</a>
</td>
<td align="left" width="63%">
Called when an object is found in the namespace during a namespace walk. Use this method as the main action function for the class implementing it. Perform your actions as needed inside this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-initializeprogressdialog">InitializeProgressDialog</a>
</td>
<td align="left" width="63%">
Initializes the window title and cancel button text of the progress dialog box displayed during the namespace walk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-leavefolder">LeaveFolder</a>
</td>
<td align="left" width="63%">
Called after a namespace walk through a folder. Use this method to perform any necessary cleanup following the actions performed by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-enterfolder">INamespaceWalkCB::EnterFolder</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inamespacewalkcb-founditem">INamespaceWalkCB::FoundItem</a>.

</td>
</tr>
</table> 


## -remarks



The IID for this interface is IID_INamespaceWalkCB.



