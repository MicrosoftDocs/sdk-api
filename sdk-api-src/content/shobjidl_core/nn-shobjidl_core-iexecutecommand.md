---
UID: NN:shobjidl_core.IExecuteCommand
title: IExecuteCommand (shobjidl_core.h)
description: Exposes methods that set a given state or parameter related to the command verb, as well as a method to invoke that verb.
old-location: shell\IExecuteCommand.htm
tech.root: shell
ms.assetid: a3432f1a-dd33-4e0d-8b26-1312bb5151f7
ms.date: 12/05/2018
ms.keywords: IExecuteCommand, IExecuteCommand interface [Windows Shell], IExecuteCommand interface [Windows Shell],described, _shell_IExecuteCommand, shell.IExecuteCommand, shobjidl_core/IExecuteCommand
ms.topic: interface
f1_keywords:
- shobjidl_core/IExecuteCommand
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExecuteCommand interface


## -description


Exposes methods that set a given state or parameter related to the command verb, as well as a method to invoke that verb.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExecuteCommand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExecuteCommand</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-execute">Execute</a>
</td>
<td align="left" width="63%">
Invoke the verb on the selected items. Call this method after you have called the other methods of this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-setdirectory">SetDirectory</a>
</td>
<td align="left" width="63%">
Sets a new working directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-setkeystate">SetKeyState</a>
</td>
<td align="left" width="63%">
Sets a value based on the current state of the keys CTRL and SHIFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-setnoshowui">SetNoShowUI</a>
</td>
<td align="left" width="63%">
Indicates whether any UI associated with the selected Shell item should be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-setparameters">SetParameters</a>
</td>
<td align="left" width="63%">
Provides parameter values for the verb.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-setposition">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the coordinates of a point used for display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-setshowwindow">SetShowWindow</a>
</td>
<td align="left" width="63%">
Sets the specified window's visual state.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface when you choose it as your method to invoke the verb to perform an action on selected items. The items are passed as a Shell item array through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithselection-setselection">IObjectWithSelection::SetSelection</a>, so the object must also implement <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection">IObjectWithSelection</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Do not call the methods of <b>IExecuteCommand</b> directly. Windows Explorer calls your <b>IExecuteCommand</b> methods when the user wants to perform an action on the items.

Note that, apart from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-execute">Execute</a>, the methods of this interface pass system information to the handler. The system itself calls these methods, setting the parameters appropriately based on system settings and conditions.



