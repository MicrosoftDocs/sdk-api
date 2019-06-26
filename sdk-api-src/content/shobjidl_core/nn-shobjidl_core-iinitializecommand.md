---
UID: NN:shobjidl_core.IInitializeCommand
title: IInitializeCommand (shobjidl_core.h)
author: windows-sdk-content
description: Exposes a single method used to initialize objects that implement IExplorerCommandState, IExecuteCommand or IDropTarget with the application-specified command name and its registered properties.
old-location: shell\IInitializeCommand.htm
tech.root: shell
ms.assetid: e5a2a4d3-2488-4da2-aaab-c27461859d9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInitializeCommand, IInitializeCommand interface [Windows Shell], IInitializeCommand interface [Windows Shell],described, _shell_IInitializeCommand, shell.IInitializeCommand, shobjidl_core/IInitializeCommand
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IInitializeCommand"
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IInitializeCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInitializeCommand interface


## -description


Exposes a single method used to initialize objects that implement <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate">IExplorerCommandState</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand">IExecuteCommand</a> or <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> with the application-specified command name and its registered properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeCommand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitializeCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializecommand-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initialize objects that share an implementation of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate">IExplorerCommandState</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand">IExecuteCommand</a> or <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> with the application-specified command name and its registered properties.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IInitializeCommand</b> in the following situations.
			    
                

<ul>
<li>Implement this interface to differentiate between related commands that share implementations of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate">IExplorerCommandState</a>, <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand">IExecuteCommand</a>. Differentiation is made through the command name passed in <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializecommand-initialize">IInitializeCommand::Initialize</a>. Commands can also use <b>Initialize</b> to pass a specific property bag for the command, using properties the command has placed in the registry.</li>
</ul>
<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Do not call the method of <b>IInitializeCommand</b> directly. Windows Explorer calls this method when a verb object that implements this interface is invoked.



