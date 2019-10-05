---
UID: NN:mmc.IExtendTaskPad
title: IExtendTaskPad (mmc.h)
author: windows-sdk-content
description: The IExtendTaskPad interface is introduced in MMC 1.1.
old-location: mmc\iextendtaskpad.htm
tech.root: mmc
ms.assetid: 30f5b526-d2d5-48a6-be5f-d0f2ba9397c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExtendTaskPad, IExtendTaskPad interface [MMC], IExtendTaskPad interface [MMC],described, _slate_iextendtaskpad, mmc.iextendtaskpad, mmc/IExtendTaskPad
ms.topic: interface
f1_keywords: 
 - "mmc/IExtendTaskPad"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtendTaskPad interface


## -description


The 
<b>IExtendTaskPad</b> interface is introduced in MMC 1.1.

The 
<b>IExtendTaskPad</b> interface enables a snap-in component to set up a taskpad and receive notifications from the taskpad.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendTaskPad</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtendTaskPad</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-enumtasks">EnumTasks</a>
</td>
<td align="left" width="63%">
Enables MMC to get a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-ienumtask">IEnumTASK</a> interface of the object that contains the snap-in's tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getbackground">GetBackground</a>
</td>
<td align="left" width="63%">
Enables MMC to get the taskpad's background image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getdescriptivetext">GetDescriptiveText</a>
</td>
<td align="left" width="63%">
Enables MMC to get the taskpad's descriptive text, which is displayed beneath the title.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getlistpadinfo">GetListPadInfo</a>
</td>
<td align="left" width="63%">
Used for list-view taskpads only. Enables MMC to get the title text for the list control, text for an optional button, and the command ID passed to <a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> when the button is clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-gettitle">GetTitle</a>
</td>
<td align="left" width="63%">
Enables MMC to get the taskpad's title text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">TaskNotify</a>
</td>
<td align="left" width="63%">
Enables MMC to notify the snap-in when a task is clicked. If the taskpad is a list-view taskpad, MMC also calls 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">TaskNotify</a> when a list-view button is clicked.

</td>
</tr>
</table> 

