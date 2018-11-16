---
UID: NN:shobjidl.IFileDialogControlEvents
title: IFileDialogControlEvents
author: windows-sdk-content
description: Exposes methods that allow an application to be notified of events that are related to controls that the application has added to a common file dialog.
old-location: shell\IFileDialogControlEvents.htm
tech.root: shell
ms.assetid: 745ee176-53bc-4388-beaa-a0856a438ee6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFileDialogControlEvents, IFileDialogControlEvents interface [Windows Shell], IFileDialogControlEvents interface [Windows Shell],described, shell.IFileDialogControlEvents, shell_IFileDialogControlEvents, shobjidl/IFileDialogControlEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
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
 - Shobjidl.h
api_name:
 - IFileDialogControlEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileDialogControlEvents interface


## -description


Exposes methods that allow an application to be notified of events that are related to controls that the application has added to a common file dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialogControlEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFileDialogControlEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileDialogControlEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46dc28a4-717f-42b6-bff7-56f4902f075c">OnButtonClicked</a>
</td>
<td align="left" width="63%">
Called when the user clicks a command button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97e6cb2a-1ffc-43ca-abb6-f1b259e8fcd2">OnCheckButtonToggled</a>
</td>
<td align="left" width="63%">
Called when the user changes the state of a check button (check box).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12efb183-65b9-4095-be57-7c7802bda2ce">OnControlActivating</a>
</td>
<td align="left" width="63%">
Called when an <b>Open</b> button drop-down list customized through <a href="https://msdn.microsoft.com/b4626030-0fc7-4329-b897-01f4ce8728a0">IFileDialogCustomize::EnableOpenDropDown</a> or a <b>Tools</b> menu is about to display its contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c96d0b7-74d1-4f87-946d-beeaad517d91">OnItemSelected</a>
</td>
<td align="left" width="63%">
Called when an item is selected in a combo box, when a user clicks an option button (also known as a radio button), or an item is chosen from the <b>Tools</b> menu.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileDialogControlEvents</b> is implemented by an application on the same object that it implements <a href="https://msdn.microsoft.com/c55107a3-ae0a-4b46-80a3-8a731b47976c">IFileDialogEvents</a> in.

The dialog does not check the return values of this interface's methods.



