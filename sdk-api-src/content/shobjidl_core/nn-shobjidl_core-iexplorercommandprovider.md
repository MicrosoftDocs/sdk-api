---
UID: NN:shobjidl_core.IExplorerCommandProvider
title: IExplorerCommandProvider
author: windows-sdk-content
description: Exposes methods to create Explorer commands and command enumerators.
old-location: shell\IExplorerCommandProvider.htm
tech.root: shell
ms.assetid: f39ea1f7-28ba-4a5e-ac19-bcfc6052fdeb
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IExplorerCommandProvider, IExplorerCommandProvider interface [Windows Shell], IExplorerCommandProvider interface [Windows Shell],described, _shell_IExplorerCommandProvider, shell.IExplorerCommandProvider, shobjidl_core/IExplorerCommandProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IExplorerCommandProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommandProvider interface


## -description


Exposes methods to create Explorer commands and command enumerators.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerCommandProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExplorerCommandProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExplorerCommandProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ef1fb9d-03ed-4e1a-bc13-9f5caab2abb9">GetCommand</a>
</td>
<td align="left" width="63%">
Gets a specified Explorer command instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df300219-e717-4f79-8996-62726092c3c7">GetCommands</a>
</td>
<td align="left" width="63%">
Gets a specified Explorer command enumerator instance.

</td>
</tr>
</table> 


## -remarks



None of the methods of this interface should communicate with network resources; they are called on the UI thread and doing so would cause the UI to stop responding.

Each command should have its own unique GUID; the command provider is expected to create a command instance on a per-GUID basis.
            



