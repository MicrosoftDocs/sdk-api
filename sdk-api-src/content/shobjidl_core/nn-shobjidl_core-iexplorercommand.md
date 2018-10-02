---
UID: NN:shobjidl_core.IExplorerCommand
title: IExplorerCommand
author: windows-sdk-content
description: Exposes methods that get the command appearance, enumerate subcommands, or invoke the command.
old-location: shell\IExplorerCommand.htm
tech.root: Shell
ms.assetid: 61e94e50-9e12-4a2c-a6c7-64a9181f80b8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IExplorerCommand, IExplorerCommand interface [Windows Shell], IExplorerCommand interface [Windows Shell],described, _shell_IExplorerCommand, shell.IExplorerCommand, shobjidl_core/IExplorerCommand
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
 - IExplorerCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerCommand interface


## -description


Exposes methods that get the command appearance, enumerate subcommands, or invoke the command.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerCommand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExplorerCommand</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c907fb46-fb18-431c-861b-c2d2270a89b9">EnumSubCommands</a>
</td>
<td align="left" width="63%">
Retrieves an enemerator for a command's subcommands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0f2fc66-98f5-404f-9d82-0290ed235ac0">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Gets the GUID of an Windows Explorer command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd0a01fa-2525-4296-b77d-bba3fb80472d">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags associated with a Windows Explorer command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e71b6748-84fc-4944-90b8-a5b0bf97079d">GetIcon</a>
</td>
<td align="left" width="63%">
Gets an icon resource string of the icon associated with the specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb600cb5-9b7e-45dc-beca-0a913c214084">GetState</a>
</td>
<td align="left" width="63%">
Gets state information associated with a specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d03ca4c5-80a5-4b7d-a47b-a67c72b7883c">GetTitle</a>
</td>
<td align="left" width="63%">
Gets the title text of the button or menu item that launches a specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2c54602-2ffc-45bc-ba00-d7b9d4cf2343">GetToolTip</a>
</td>
<td align="left" width="63%">
Gets the tooltip string associated with a specified Windows Explorer command item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ea545a4-5f4c-4f98-9e56-b7c7eed5f821">Invoke</a>
</td>
<td align="left" width="63%">
Invokes a Windows Explorer command.

</td>
</tr>
</table> 


## -remarks



None of the methods of this interface should communicate with network resources. These methods are called on the UI thread, so communication with network resources could cause the UI to stop responding.



