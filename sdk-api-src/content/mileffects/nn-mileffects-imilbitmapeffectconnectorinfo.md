---
UID: NN:mileffects.IMILBitmapEffectConnectorInfo
title: IMILBitmapEffectConnectorInfo (mileffects.h)

description: Exposes methods that retrieve information about a specific input or output connector pin.
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\imilbitmapeffectconnectorinfo.htm

ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectConnectorInfo, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects], IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnectorinfo, mileffects/IMILBitmapEffectConnectorInfo, wibe._wibe_imilbitmapeffectconnectorinfo
ms.topic: interface
f1_keywords: 
 - "mileffects/IMILBitmapEffectConnectorInfo"
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
 - IMILBitmapEffectConnectorInfo
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectConnectorInfo interface


## -description


Exposes methods that retrieve information about a specific input or output connector pin.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnectorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectConnectorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectConnectorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnectorinfo-getformat">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format for the given pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms735300(v=vs.85)">GetIndex</a>
</td>
<td align="left" width="63%">
Retrieves the zero based index value for the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnectorinfo-getnumberformats">GetNumberFormats</a>
</td>
<td align="left" width="63%">
Retrieves the number of pixel formats supported by the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectconnectorinfo-getoptimalformat">GetOptimalFormat</a>
</td>
<td align="left" width="63%">
Retrieves the optimal pixel format for the pin.

</td>
</tr>
</table> 

