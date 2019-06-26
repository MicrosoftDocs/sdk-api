---
UID: NN:mmc.IControlbar
title: IControlbar (mmc.h)
author: windows-sdk-content
description: The IControlbar interface provides a way to create toolbars and other controls.
old-location: mmc\icontrolbar.htm
tech.root: mmc
ms.assetid: 8ba12331-34e8-46ff-ab66-a6ada3d731f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IControlbar, IControlbar interface [MMC], IControlbar interface [MMC],described, _slate_icontrolbar, mmc.icontrolbar, mmc/IControlbar
ms.topic: interface
f1_keywords: 
 - "mmc/IControlbar"
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
ms.custom: 19H1
---

# IControlbar interface


## -description


The 
<b>IControlbar</b> interface provides a way to create toolbars and other controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IControlbar</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IControlbar</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontrolbar-attach">Attach</a>
</td>
<td align="left" width="63%">
Associates a control with a control bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontrolbar-create">Create</a>
</td>
<td align="left" width="63%">
Creates and returns a control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icontrolbar-detach">Detach</a>
</td>
<td align="left" width="63%">
Removes a control from a control bar.

</td>
</tr>
</table> 

