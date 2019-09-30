---
UID: NN:mileffects.IMILBitmapEffectConnector
title: IMILBitmapEffectConnector (mileffects.h)
author: windows-sdk-content
description: Exposes methods that define an effect output pin.
old-location: wibe\_wibe_imilbitmapeffectconnector.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnector\imilbitmapeffectconnector.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectConnector, IMILBitmapEffectConnector interface [WPF Bitmap Effects], IMILBitmapEffectConnector interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnector, mileffects/IMILBitmapEffectConnector, wibe._wibe_imilbitmapeffectconnector
ms.topic: interface
f1_keywords: 
 - "mileffects/IMILBitmapEffectConnector"
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
 - IMILBitmapEffectConnector
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectConnector interface


## -description


Exposes methods that define an effect output pin.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectConnector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectConnector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnector-getbitmapeffect">GetBitmapEffect</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a> associated with the connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnector-isconnected">IsConnected</a>
</td>
<td align="left" width="63%">
Determines whether the connector is connected to an effect.

</td>
</tr>
</table> 

