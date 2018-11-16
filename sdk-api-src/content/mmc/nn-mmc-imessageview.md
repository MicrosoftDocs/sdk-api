---
UID: NN:mmc.IMessageView
title: IMessageView
author: windows-sdk-content
description: The IMessageView interface is introduced in MMC 1.2.
old-location: mmc\imessageview.htm
tech.root: MMC
ms.assetid: e1ea6bb2-f35e-4379-b4e4-70d4e5d77b93
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMessageView, IMessageView interface [MMC], IMessageView interface [MMC],described, _slate_imessageview, mmc.imessageview, mmc/IMessageView
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
 - IMessageView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMessageView interface


## -description


The 
<b>IMessageView</b> interface is introduced in MMC 1.2.

The 
<b>IMessageView</b> interface provides support for specifying the text and icons for error messages displayed using the MMC message OCX control. For details on using the control, see 
<a href="https://msdn.microsoft.com/bc6db308-d8dd-4868-803d-45c64b951192">Using the MMC Message OCX Control</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMessageView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMessageView</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/495b92bf-1629-49f5-917c-290151c9176e">Clear</a>
</td>
<td align="left" width="63%">
Clears the title, text, and icon of the result pane message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27b3ae83-be3c-4d40-88b8-9253f1c793f6">SetBodyText</a>
</td>
<td align="left" width="63%">
Changes the text for the result pane message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61389d5b-cf0a-465e-9b3b-1bcdef4f92b1">SetIcon</a>
</td>
<td align="left" width="63%">
Changes the icon for the result pane message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e041cf74-9fdd-489c-a251-e5b3e55e1bc5">SetTitleText</a>
</td>
<td align="left" width="63%">
Changes the title for the result pane message.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bc6db308-d8dd-4868-803d-45c64b951192">Using the MMC Message OCX Control</a>
 

 

