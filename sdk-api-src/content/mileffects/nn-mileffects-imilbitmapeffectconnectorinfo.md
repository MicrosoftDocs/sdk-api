---
UID: NN:mileffects.IMILBitmapEffectConnectorInfo
title: IMILBitmapEffectConnectorInfo
author: windows-sdk-content
description: Exposes methods that retrieve information about a specific input or output connector pin.
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\imilbitmapeffectconnectorinfo.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: IMILBitmapEffectConnectorInfo, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects], IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnectorinfo, mileffects/IMILBitmapEffectConnectorInfo, wibe._wibe_imilbitmapeffectconnectorinfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectConnectorInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/bf0beb64-f26a-45e1-ad4a-5d11127a516f">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the pixel format for the given pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da4bee4c-8263-46f2-a265-71bdd1f69b0c">GetIndex</a>
</td>
<td align="left" width="63%">
Retrieves the zero based index value for the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b589f382-1c1c-4537-9815-d262e10173a4">GetNumberFormats</a>
</td>
<td align="left" width="63%">
Retrieves the number of pixel formats supported by the pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f670662-c58c-4b1d-b7b6-c766b9fa8692">GetOptimalFormat</a>
</td>
<td align="left" width="63%">
Retrieves the optimal pixel format for the pin.

</td>
</tr>
</table> 

