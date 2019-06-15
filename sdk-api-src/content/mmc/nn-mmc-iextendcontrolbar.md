---
UID: NN:mmc.IExtendControlbar
title: IExtendControlbar (mmc.h)
author: windows-sdk-content
description: The IExtendControlbar interface enables an extension to add control bars to the console. This provides a way to improve the functionality and appearance of your snap-in by adding toolbars or other user interface enhancements.
old-location: mmc\iextendcontrolbar.htm
tech.root: mmc
ms.assetid: e0d586e3-5ad9-4996-b5bd-d6ab4f2eaf26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExtendControlbar, IExtendControlbar interface [MMC], IExtendControlbar interface [MMC],described, _slate_iextendcontrolbar, mmc.iextendcontrolbar, mmc/IExtendControlbar
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
 - IExtendControlbar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtendControlbar interface


## -description


The 
<b>IExtendControlbar</b> interface enables an extension to add control bars to the console. This provides a way to improve the functionality and appearance of your snap-in by adding toolbars or other user interface enhancements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendControlbar</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtendControlbar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendControlbar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendcontrolbar-controlbarnotify">ControlbarNotify</a>
</td>
<td align="left" width="63%">
A value that specifies notifications resulting from user actions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendcontrolbar-setcontrolbar">SetControlbar</a>
</td>
<td align="left" width="63%">
Attaches or detaches the control bar.

</td>
</tr>
</table> 

