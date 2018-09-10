---
UID: NN:mmc.IExtendTaskPad
title: IExtendTaskPad
author: windows-sdk-content
description: The IExtendTaskPad interface is introduced in MMC 1.1.
old-location: mmc\iextendtaskpad.htm
tech.root: mmc
ms.assetid: 30f5b526-d2d5-48a6-be5f-d0f2ba9397c4
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IExtendTaskPad, IExtendTaskPad interface [MMC], IExtendTaskPad interface [MMC],described, _slate_iextendtaskpad, mmc.iextendtaskpad, mmc/IExtendTaskPad
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Mmc.h
api_name:
 - IExtendTaskPad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExtendTaskPad interface


## -description


The 
<b>IExtendTaskPad</b> interface is introduced in MMC 1.1.

The 
<b>IExtendTaskPad</b> interface enables a snap-in component to set up a taskpad and receive notifications from the taskpad.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendTaskPad</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExtendTaskPad</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendTaskPad</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5faced6f-68aa-453e-b5da-99b79e9c8e15">EnumTasks</a>
</td>
<td align="left" width="63%">
Enables MMC to get a pointer to the 
<a href="https://msdn.microsoft.com/7cf1ff4f-bd45-4ead-a005-e0f38aed9039">IEnumTASK</a> interface of the object that contains the snap-in's tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e34fc088-61d7-46a8-b493-8255a733d521">GetBackground</a>
</td>
<td align="left" width="63%">
Enables MMC to get the taskpad's background image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8d02b4e-703f-42fe-a55c-cc5cf84e8f74">GetDescriptiveText</a>
</td>
<td align="left" width="63%">
Enables MMC to get the taskpad's descriptive text, which is displayed beneath the title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73e9d281-9bf9-4a50-b3e8-226ed3593f7a">GetListPadInfo</a>
</td>
<td align="left" width="63%">
Used for list-view taskpads only. Enables MMC to get the title text for the list control, text for an optional button, and the command ID passed to <a href="https://msdn.microsoft.com/c20d87f9-a5a0-41b9-b343-a11e8b41ed71">IExtendTaskPad::TaskNotify</a> when the button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d04eb4fe-bcb2-457f-8d22-434352068056">GetTitle</a>
</td>
<td align="left" width="63%">
Enables MMC to get the taskpad's title text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c20d87f9-a5a0-41b9-b343-a11e8b41ed71">TaskNotify</a>
</td>
<td align="left" width="63%">
Enables MMC to notify the snap-in when a task is clicked. If the taskpad is a list-view taskpad, MMC also calls 
<a href="https://msdn.microsoft.com/c20d87f9-a5a0-41b9-b343-a11e8b41ed71">TaskNotify</a> when a list-view button is clicked.

</td>
</tr>
</table> 

