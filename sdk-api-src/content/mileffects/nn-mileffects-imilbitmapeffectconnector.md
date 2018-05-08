---
UID: NN:mileffects.IMILBitmapEffectConnector
title: IMILBitmapEffectConnector
author: windows-driver-content
description: Exposes methods that define an effect output pin.
old-location: wibe\_wibe_imilbitmapeffectconnector.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnector\imilbitmapeffectconnector.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IMILBitmapEffectConnector, IMILBitmapEffectConnector interface [WPF Bitmap Effects], IMILBitmapEffectConnector interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnector, mileffects/IMILBitmapEffectConnector, wibe._wibe_imilbitmapeffectconnector
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.dll
api_name:
-	IMILBitmapEffectConnector
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnector interface


## -description


Exposes methods that define an effect output pin.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectConnector</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/00abf251-81a1-41de-bf0e-9ea77f0ac5f0">GetBitmapEffect</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a> associated with the connector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42ecc47d-cfea-41b8-bc0c-f346a9e18611">IsConnected</a>
</td>
<td align="left" width="63%">
Determines whether the connector is connected to an effect.

</td>
</tr>
</table> 

