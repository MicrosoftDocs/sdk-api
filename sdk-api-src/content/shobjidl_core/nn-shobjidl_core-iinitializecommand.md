---
UID: NN:shobjidl_core.IInitializeCommand
title: IInitializeCommand
author: windows-sdk-content
description: Exposes a single method used to initialize objects that implement IExplorerCommandState, IExecuteCommand or IDropTarget with the application-specified command name and its registered properties.
old-location: shell\IInitializeCommand.htm
old-project: shell
ms.assetid: e5a2a4d3-2488-4da2-aaab-c27461859d9f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IInitializeCommand, IInitializeCommand interface [Windows Shell], IInitializeCommand interface [Windows Shell],described, _shell_IInitializeCommand, shell.IInitializeCommand, shobjidl_core/IInitializeCommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IInitializeCommand interface


## -description


Exposes a single method used to initialize objects that implement <a href="https://msdn.microsoft.com/020a6f6f-1d45-44bd-a57f-ef8000976b5b">IExplorerCommandState</a>, <a href="https://msdn.microsoft.com/a3432f1a-dd33-4e0d-8b26-1312bb5151f7">IExecuteCommand</a> or <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> with the application-specified command name and its registered properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeCommand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInitializeCommand</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initialize objects that share an implementation of <a href="https://msdn.microsoft.com/020a6f6f-1d45-44bd-a57f-ef8000976b5b">IExplorerCommandState</a>, <a href="https://msdn.microsoft.com/a3432f1a-dd33-4e0d-8b26-1312bb5151f7">IExecuteCommand</a> or <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> with the application-specified command name and its registered properties.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IInitializeCommand</b> in the following situations.
			    
                

<ul>
<li>Implement this interface to differentiate between related commands that share implementations of <a href="https://msdn.microsoft.com/020a6f6f-1d45-44bd-a57f-ef8000976b5b">IExplorerCommandState</a>, <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> or <a href="https://msdn.microsoft.com/a3432f1a-dd33-4e0d-8b26-1312bb5151f7">IExecuteCommand</a>. Differentiation is made through the command name passed in <a href="https://msdn.microsoft.com/ec115bee-7ce3-428b-9081-2f21f3793de4">IInitializeCommand::Initialize</a>. Commands can also use <b>Initialize</b> to pass a specific property bag for the command, using properties the command has placed in the registry.</li>
</ul>
<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Do not call the method of <b>IInitializeCommand</b> directly. Windows Explorer calls this method when a verb object that implements this interface is invoked.



