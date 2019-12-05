---
UID: NN:mmc.IMessageView
title: IMessageView (mmc.h)
description: The IMessageView interface is introduced in MMC 1.2.
old-location: mmc\imessageview.htm
tech.root: mmc
ms.assetid: e1ea6bb2-f35e-4379-b4e4-70d4e5d77b93
ms.date: 12/05/2018
ms.keywords: IMessageView, IMessageView interface [MMC], IMessageView interface [MMC],described, _slate_imessageview, mmc.imessageview, mmc/IMessageView
ms.topic: interface
f1_keywords:
- mmc/IMessageView
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
- IMessageView
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMessageView interface


## -description


The 
<b>IMessageView</b> interface is introduced in MMC 1.2.

The 
<b>IMessageView</b> interface provides support for specifying the text and icons for error messages displayed using the MMC message OCX control. For details on using the control, see 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMessageView</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMessageView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMessageView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-imessageview-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the title, text, and icon of the result pane message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-imessageview-setbodytext">SetBodyText</a>
</td>
<td align="left" width="63%">
Changes the text for the result pane message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-imessageview-seticon">SetIcon</a>
</td>
<td align="left" width="63%">
Changes the icon for the result pane message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-imessageview-settitletext">SetTitleText</a>
</td>
<td align="left" width="63%">
Changes the title for the result pane message.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>
 

 

