---
UID: NN:mileffects.IMILBitmapEffectConnections
title: IMILBitmapEffectConnections (mileffects.h)
description: Exposes methods used to retrieve input and output connectors exposed by the bitmap effect.helpviewer_keywords: ["IMILBitmapEffectConnections","IMILBitmapEffectConnections interface [WPF Bitmap Effects]","IMILBitmapEffectConnections interface [WPF Bitmap Effects]","described","_wibe_imilbitmapeffectconnections","mileffects/IMILBitmapEffectConnections","wibe._wibe_imilbitmapeffectconnections"]
old-location: wibe\_wibe_imilbitmapeffectconnections.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnections\imilbitmapeffectconnections.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectConnections, IMILBitmapEffectConnections interface [WPF Bitmap Effects], IMILBitmapEffectConnections interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnections, mileffects/IMILBitmapEffectConnections, wibe._wibe_imilbitmapeffectconnections
f1_keywords:
- mileffects/IMILBitmapEffectConnections
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mileffects.h
api_name:
- IMILBitmapEffectConnections
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectConnections interface


## -description


Exposes methods used to retrieve input and output connectors exposed by the bitmap effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnections</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectConnections</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectConnections</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnections-getinputconnector">GetInputConnector</a>
</td>
<td align="left" width="63%">
Retrieves the input connector associated with the given pin index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnections-getoutputconnector">GetOutputConnector</a>
</td>
<td align="left" width="63%">
Retrieves the output connector associated with the given pin index.

</td>
</tr>
</table> 

