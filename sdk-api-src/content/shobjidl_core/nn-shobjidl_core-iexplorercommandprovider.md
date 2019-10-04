---
UID: NN:shobjidl_core.IExplorerCommandProvider
title: IExplorerCommandProvider (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods to create Explorer commands and command enumerators.
old-location: shell\IExplorerCommandProvider.htm
tech.root: shell
ms.assetid: f39ea1f7-28ba-4a5e-ac19-bcfc6052fdeb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExplorerCommandProvider, IExplorerCommandProvider interface [Windows Shell], IExplorerCommandProvider interface [Windows Shell],described, _shell_IExplorerCommandProvider, shell.IExplorerCommandProvider, shobjidl_core/IExplorerCommandProvider
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IExplorerCommandProvider"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerCommandProvider interface


## -description


Exposes methods to create Explorer commands and command enumerators.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerCommandProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerCommandProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommandprovider-getcommand">GetCommand</a>
</td>
<td align="left" width="63%">
Gets a specified Explorer command instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommandprovider-getcommands">GetCommands</a>
</td>
<td align="left" width="63%">
Gets a specified Explorer command enumerator instance.

</td>
</tr>
</table> 


## -remarks



None of the methods of this interface should communicate with network resources; they are called on the UI thread and doing so would cause the UI to stop responding.

Each command should have its own unique GUID; the command provider is expected to create a command instance on a per-GUID basis.
            



