---
UID: NN:mmc.IToolbar
title: IToolbar
author: windows-sdk-content
description: The IToolbar interface is used to create new toolbars, to add items to them, to extend the toolbars, and to display the resultant new toolbars. Each toolbar is created on its own band within the control bar.
old-location: mmc\itoolbar.htm
tech.root: mmc
ms.assetid: cf9c9fe9-f58f-47f0-9051-86a514df0c6d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IToolbar, IToolbar interface [MMC], IToolbar interface [MMC],described, _slate_itoolbar, mmc.itoolbar, mmc/IToolbar
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IToolbar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToolbar interface


## -description


The 
<b>IToolbar</b> interface is used to create new toolbars, to add items to them, to extend the toolbars, and to display the resultant new toolbars. Each toolbar is created on its own band within the control bar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IToolbar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IToolbar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IToolbar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2ef31a7-61ce-4ac6-814a-c3a46964c4f1">AddBitmap</a>
</td>
<td align="left" width="63%">
Adds an image to the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d37d0bc-d7c3-4d23-8dd4-c5a6c4af15ee">AddButtons</a>
</td>
<td align="left" width="63%">
Adds an array of buttons to the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c893b3a6-a0f8-42ce-bf82-2e45f6458500">DeleteButton</a>
</td>
<td align="left" width="63%">
Removes a button from the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94c41b13-f1ab-4368-8cfa-960caeea796e">GetButtonState</a>
</td>
<td align="left" width="63%">
Gets an attribute of a button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/768df6d0-c2e5-4099-b4a6-a71e4f7e06d7">InsertButton</a>
</td>
<td align="left" width="63%">
Adds a single button to the toolbar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa43fc1b-cc6d-474d-9b92-556924fb98de">SetButtonState</a>
</td>
<td align="left" width="63%">
Sets an attribute of a button.

</td>
</tr>
</table> 

