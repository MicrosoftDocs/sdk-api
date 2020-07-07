---
UID: NN:mileffects.IMILBitmapEffectInputConnector
title: IMILBitmapEffectInputConnector (mileffects.h)
description: Exposes methods that define an input connect.
helpviewer_keywords: ["IMILBitmapEffectInputConnector","IMILBitmapEffectInputConnector interface [WPF Bitmap Effects]","IMILBitmapEffectInputConnector interface [WPF Bitmap Effects]","described","_wibe_imilbitmapeffectinputconnector","mileffects/IMILBitmapEffectInputConnector","wibe._wibe_imilbitmapeffectinputconnector"]
old-location: wibe\_wibe_imilbitmapeffectinputconnector.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectinputconnector\imilbitmapeffectinputconnector.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectInputConnector, IMILBitmapEffectInputConnector interface [WPF Bitmap Effects], IMILBitmapEffectInputConnector interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectinputconnector, mileffects/IMILBitmapEffectInputConnector, wibe._wibe_imilbitmapeffectinputconnector
f1_keywords:
- mileffects/IMILBitmapEffectInputConnector
dev_langs:
- c++
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mileffects.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mileffects.dll
api_name:
- IMILBitmapEffectInputConnector
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectInputConnector interface


## -description


Exposes methods that define an input connect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectInputConnector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectInputConnector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectInputConnector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectinputconnector-connectto">ConnectTo</a>
</td>
<td align="left" width="63%">
Connects the input connector to the given output connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectinputconnector-getconnection">GetConnection</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectoutputconnector">IMILBitmapEffectOutputConnector</a> the input connector is connected to.

</td>
</tr>
</table> 

