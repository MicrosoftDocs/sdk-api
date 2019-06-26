---
UID: NN:shobjidl_core.IExplorerCommand
title: IExplorerCommand (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that get the command appearance, enumerate subcommands, or invoke the command.
old-location: shell\IExplorerCommand.htm
tech.root: shell
ms.assetid: 61e94e50-9e12-4a2c-a6c7-64a9181f80b8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExplorerCommand, IExplorerCommand interface [Windows Shell], IExplorerCommand interface [Windows Shell],described, _shell_IExplorerCommand, shell.IExplorerCommand, shobjidl_core/IExplorerCommand
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IExplorerCommand"
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
 - IExplorerCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerCommand interface


## -description


Exposes methods that get the command appearance, enumerate subcommands, or invoke the command.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerCommand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExplorerCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands">EnumSubCommands</a>
</td>
<td align="left" width="63%">
Retrieves an enemerator for a command's subcommands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Gets the GUID of an Windows Explorer command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags associated with a Windows Explorer command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-geticon">GetIcon</a>
</td>
<td align="left" width="63%">
Gets an icon resource string of the icon associated with the specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getstate">GetState</a>
</td>
<td align="left" width="63%">
Gets state information associated with a specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-gettitle">GetTitle</a>
</td>
<td align="left" width="63%">
Gets the title text of the button or menu item that launches a specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-gettooltip">GetToolTip</a>
</td>
<td align="left" width="63%">
Gets the tooltip string associated with a specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Invokes a Windows Explorer command.

</td>
</tr>
</table> 


## -remarks



None of the methods of this interface should communicate with network resources. These methods are called on the UI thread, so communication with network resources could cause the UI to stop responding.



