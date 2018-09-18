---
UID: NN:shobjidl_core.IExecuteCommand
title: IExecuteCommand
author: windows-sdk-content
description: Exposes methods that set a given state or parameter related to the command verb, as well as a method to invoke that verb.
old-location: shell\IExecuteCommand.htm
tech.root: shell
ms.assetid: a3432f1a-dd33-4e0d-8b26-1312bb5151f7
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IExecuteCommand, IExecuteCommand interface [Windows Shell], IExecuteCommand interface [Windows Shell],described, _shell_IExecuteCommand, shell.IExecuteCommand, shobjidl_core/IExecuteCommand
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
 - IExecuteCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExecuteCommand interface


## -description


Exposes methods that set a given state or parameter related to the command verb, as well as a method to invoke that verb.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExecuteCommand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExecuteCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExecuteCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/388136bb-a5c0-48c0-adfc-f5154910fd72">Execute</a>
</td>
<td align="left" width="63%">
Invoke the verb on the selected items. Call this method after you have called the other methods of this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8416b2ef-8e62-4679-adc1-ec953875db34">SetDirectory</a>
</td>
<td align="left" width="63%">
Sets a new working directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f051a1-eb45-43c1-bf09-4be6ca2a1c7c">SetKeyState</a>
</td>
<td align="left" width="63%">
Sets a value based on the current state of the keys CTRL and SHIFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26cec8f2-984a-4358-9082-bf6b886690eb">SetNoShowUI</a>
</td>
<td align="left" width="63%">
Indicates whether any UI associated with the selected Shell item should be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e08777c-865b-49c2-8f37-1a427c4945b4">SetParameters</a>
</td>
<td align="left" width="63%">
Provides parameter values for the verb.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ead12c05-ce94-494d-9f31-9b0f341363b5">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the coordinates of a point used for display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57ac201e-0680-4856-ab05-9f8b49aecd62">SetShowWindow</a>
</td>
<td align="left" width="63%">
Sets the specified window's visual state.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface when you choose it as your method to invoke the verb to perform an action on selected items. The items are passed as a Shell item array through <a href="https://msdn.microsoft.com/e561b8f8-36e9-45ec-beb2-62d7f429dec4">IObjectWithSelection::SetSelection</a>, so the object must also implement <a href="https://msdn.microsoft.com/8fb248eb-73e7-4db0-8585-4accafe332d0">IObjectWithSelection</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Do not call the methods of <b>IExecuteCommand</b> directly. Windows Explorer calls your <b>IExecuteCommand</b> methods when the user wants to perform an action on the items.

Note that, apart from <a href="https://msdn.microsoft.com/388136bb-a5c0-48c0-adfc-f5154910fd72">Execute</a>, the methods of this interface pass system information to the handler. The system itself calls these methods, setting the parameters appropriately based on system settings and conditions.



