---
UID: NN:mileffects.IMILBitmapEffectConnectionsInfo
title: IMILBitmapEffectConnectionsInfo (mileffects.h)
author: windows-sdk-content
description: Exposes methods that retrieves information about what input and output pins are exposed by the bitmap effect.
old-location: wibe\_wibe_imilbitmapeffectconnectionsinfo.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectionsinfo\imilbitmapeffectconnectionsinfo.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectConnectionsInfo, IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects], IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnectionsinfo, mileffects/IMILBitmapEffectConnectionsInfo, wibe._wibe_imilbitmapeffectconnectionsinfo
ms.topic: interface
f1_keywords: 
 - "mileffects/IMILBitmapEffectConnectionsInfo"
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
 - IMILBitmapEffectConnectionsInfo
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectConnectionsInfo interface


## -description


Exposes methods that retrieves information about what input and output pins are exposed by the bitmap effect. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnectionsInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectConnectionsInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectConnectionsInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnectionsinfo-getinputconnectorinfo">GetInputConnectorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a> associated with the given input pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnectionsinfo-getnumberinputs">GetNumberInputs</a>
</td>
<td align="left" width="63%">
Retrieves the number of input pins the bitmap effect implements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnectionsinfo-getnumberoutputs">GetNumberOutputs</a>
</td>
<td align="left" width="63%">
Retrieves the number of output pins the bitmap effect implements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnectionsinfo-getoutputconnectorinfo">GetOutputConnectorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a> associated with the given output pin.

</td>
</tr>
</table> 


## -remarks



If this interface is not implemented when creating a custom bitmap effect, a single input and output pin implementation with a 32bit RGBA format is assumes.



