---
UID: NN:mmc.IMenuButton
title: IMenuButton
author: windows-sdk-content
description: The IMenuButton interface enables the user to add and manage menu buttons for a snap-in.
old-location: mmc\imenubutton.htm
old-project: mmc
ms.assetid: 51bbd98a-7017-497a-858a-dd63cefc679a
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IMenuButton, IMenuButton interface [MMC], IMenuButton interface [MMC],described, _slate_imenubutton, mmc.imenubutton, mmc/IMenuButton
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IMenuButton
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMenuButton interface


## -description


The 
<b>IMenuButton</b> interface enables the user to add and manage menu buttons for a snap-in. MMC provides one menu bar per view; when a snap-in has the focus you can add one or more menu buttons for the view to this bar. These buttons are always added by appending them to the buttons already in the menu bar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMenuButton</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMenuButton</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMenuButton</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75d19e2a-0d3e-4883-852e-983fcee8166a">AddButton</a>
</td>
<td align="left" width="63%">
Adds a button to the menu bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0297c54-7aa2-497b-9fe7-1be4fc7517f9">SetButton</a>
</td>
<td align="left" width="63%">
Sets the attributes of a menu bar button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28f4faf7-9fb2-4be0-84b6-e3e8f7450c34">SetButtonState</a>
</td>
<td align="left" width="63%">
Sets the state of a menu bar button.

</td>
</tr>
</table> 

