---
UID: NN:shobjidl.ITrayDeskBand
title: ITrayDeskBand
author: windows-driver-content
description: Exposes methods that show, hide, and query deskbands.
old-location: shell\ITrayDeskBand.htm
old-project: shell
ms.assetid: 4542bd20-b7ca-4ab9-9c25-9f6eeabd7c2e
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ITrayDeskBand, ITrayDeskBand interface [Windows Shell], ITrayDeskBand interface [Windows Shell],described, _shell_ITrayDeskBand, shell.ITrayDeskBand, shobjidl/ITrayDeskBand
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
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	ITrayDeskBand
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# ITrayDeskBand interface


## -description


Exposes methods that show, hide, and query deskbands.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITrayDeskBand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITrayDeskBand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITrayDeskBand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/912ae157-984e-4255-ac1e-e1e7b0b92c15">DeskBandRegistrationChanged</a>
</td>
<td align="left" width="63%">
Refreshes the deskband registration cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/586ead4b-94fe-4da1-b78e-d4f1c61b9ee2">HideDeskBand</a>
</td>
<td align="left" width="63%">
Hides a specified deskband.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/969b8a91-6685-4fd8-95a1-bb9f0bfc88b5">IsDeskBandShown</a>
</td>
<td align="left" width="63%">
Indicates whether a deskband is shown.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fd46acd-47b3-46dd-955d-c036995dd01b">ShowDeskBand</a>
</td>
<td align="left" width="63%">
Shows a specified deskband.

</td>
</tr>
</table> 

