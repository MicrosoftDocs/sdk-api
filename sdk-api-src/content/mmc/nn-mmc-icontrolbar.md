---
UID: NN:mmc.IControlbar
title: IControlbar
author: windows-sdk-content
description: The IControlbar interface provides a way to create toolbars and other controls.
old-location: mmc\icontrolbar.htm
tech.root: MMC
ms.assetid: 8ba12331-34e8-46ff-ab66-a6ada3d731f6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IControlbar, IControlbar interface [MMC], IControlbar interface [MMC],described, _slate_icontrolbar, mmc.icontrolbar, mmc/IControlbar
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
 - IControlbar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IControlbar interface


## -description


The 
<b>IControlbar</b> interface provides a way to create toolbars and other controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IControlbar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IControlbar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IControlbar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60ed8f9a-d5ad-4a68-8019-6887104c9b2a">Attach</a>
</td>
<td align="left" width="63%">
Associates a control with a control bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ce92539-f5dc-44c3-94e5-253fc9995932">Create</a>
</td>
<td align="left" width="63%">
Creates and returns a control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a40fc3a4-40ff-4752-abd9-e4dd906bc27f">Detach</a>
</td>
<td align="left" width="63%">
Removes a control from a control bar.

</td>
</tr>
</table> 

