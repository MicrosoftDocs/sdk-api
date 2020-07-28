---
UID: NN:shobjidl.ITrayDeskBand
title: ITrayDeskBand (shobjidl.h)
description: Exposes methods that show, hide, and query deskbands.
helpviewer_keywords: ["ITrayDeskBand","ITrayDeskBand interface [Windows Shell]","ITrayDeskBand interface [Windows Shell]","described","_shell_ITrayDeskBand","shell.ITrayDeskBand","shobjidl/ITrayDeskBand"]
old-location: shell\ITrayDeskBand.htm
tech.root: shell
ms.assetid: 4542bd20-b7ca-4ab9-9c25-9f6eeabd7c2e
ms.date: 12/05/2018
ms.keywords: ITrayDeskBand, ITrayDeskBand interface [Windows Shell], ITrayDeskBand interface [Windows Shell],described, _shell_ITrayDeskBand, shell.ITrayDeskBand, shobjidl/ITrayDeskBand
f1_keywords:
- shobjidl/ITrayDeskBand
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- ITrayDeskBand
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITrayDeskBand interface


## -description


Exposes methods that show, hide, and query deskbands.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITrayDeskBand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITrayDeskBand</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-itraydeskband-deskbandregistrationchanged">DeskBandRegistrationChanged</a>
</td>
<td align="left" width="63%">
Refreshes the deskband registration cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-itraydeskband-hidedeskband">HideDeskBand</a>
</td>
<td align="left" width="63%">
Hides a specified deskband.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-itraydeskband-isdeskbandshown">IsDeskBandShown</a>
</td>
<td align="left" width="63%">
Indicates whether a deskband is shown.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-itraydeskband-showdeskband">ShowDeskBand</a>
</td>
<td align="left" width="63%">
Shows a specified deskband.

</td>
</tr>
</table> 

