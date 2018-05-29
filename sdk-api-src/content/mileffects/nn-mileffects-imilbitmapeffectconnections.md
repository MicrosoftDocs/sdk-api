---
UID: NN:mileffects.IMILBitmapEffectConnections
title: IMILBitmapEffectConnections
author: windows-sdk-content
description: Exposes methods used to retrieve input and output connectors exposed by the bitmap effect.
old-location: wibe\_wibe_imilbitmapeffectconnections.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnections\imilbitmapeffectconnections.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: IMILBitmapEffectConnections, IMILBitmapEffectConnections interface [WPF Bitmap Effects], IMILBitmapEffectConnections interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnections, mileffects/IMILBitmapEffectConnections, wibe._wibe_imilbitmapeffectconnections
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectConnections
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnections interface


## -description


Exposes methods used to retrieve input and output connectors exposed by the bitmap effect.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectConnections</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectConnections</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/96f8b4e5-2c51-40c6-8081-3703fce98fb9">GetInputConnector</a>
</td>
<td align="left" width="63%">
Retrieves the input connector associated with the given pin index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2449e385-5c70-426f-80d0-ec24b35a3067">GetOutputConnector</a>
</td>
<td align="left" width="63%">
Retrieves the output connector associated with the given pin index.

</td>
</tr>
</table> 

