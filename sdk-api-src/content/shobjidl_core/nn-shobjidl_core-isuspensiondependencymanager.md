---
UID: NN:shobjidl_core.ISuspensionDependencyManager
title: ISuspensionDependencyManager (shobjidl_core.h)
description: .
old-location: shell\ISuspensionDependencyManager.htm
tech.root: shell
ms.assetid: F632DC0B-01EF-4421-ADF3-2CD5AD363CC0
ms.date: 12/05/2018
ms.keywords: ISuspensionDependencyManager, ISuspensionDependencyManager interface [Windows Shell], ISuspensionDependencyManager interface [Windows Shell],described, shell.ISuspensionDependencyManager, shobjidl_core/ISuspensionDependencyManager
f1_keywords:
- shobjidl_core/ISuspensionDependencyManager
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- ISuspensionDependencyManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISuspensionDependencyManager interface


## -description

Exposes methods to manage dependencies in process suspension scenarios. This interface is no longer supported on Windows 10, version 1809, and later versions.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISuspensionDependencyManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISuspensionDependencyManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISuspensionDependencyManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isuspensiondependencymanager-groupchildwithparent">GroupChildWithParent</a>
</td>
<td align="left" width="63%">Groups the specified child process with the parent process.</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isuspensiondependencymanager-registeraschild">RegisterAsChild</a>
</td>
<td align="left" width="63%">Registers the specified process as a child.</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isuspensiondependencymanager-ungroupchildfromparent">UngroupChildFromParent</a>
</td>
<td align="left" width="63%">Ungroups the specified child process from the parent process.</td>
</tr>
</table> 



