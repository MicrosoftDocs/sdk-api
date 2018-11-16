---
UID: NN:mileffects.IMILBitmapEffectConnectorInfo
title: IMILBitmapEffectConnectorInfo
author: windows-sdk-content
description: Exposes methods that retrieve information about a specific input or output connector pin.
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\imilbitmapeffectconnectorinfo.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMILBitmapEffectConnectorInfo, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects], IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnectorinfo, mileffects/IMILBitmapEffectConnectorInfo, wibe._wibe_imilbitmapeffectconnectorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffectConnectorInfo interface


## -description


Exposes methods that retrieve information about a specific input or output connector pin.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnectorInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectConnectorInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms735299(v=VS.85).aspx">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format for the given pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735300(v=VS.85).aspx">GetIndex</a>
</td>
<td align="left" width="63%">
Retrieves the zero based index value for the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735301(v=VS.85).aspx">GetNumberFormats</a>
</td>
<td align="left" width="63%">
Retrieves the number of pixel formats supported by the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms735302(v=VS.85).aspx">GetOptimalFormat</a>
</td>
<td align="left" width="63%">
Retrieves the optimal pixel format for the pin.

</td>
</tr>
</table> 

