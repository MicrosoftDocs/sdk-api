---
UID: NN:tuner.ITunerCap
title: ITunerCap
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The ITunerCap interface provides information about the capabilities of a BDA device filter that represents a TV tuner.
old-location: mstv\itunercap.htm
old-project: mstv
ms.assetid: d7027ff4-4fb9-48c1-b527-92e65009b089
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITunerCap, ITunerCap interface [Microsoft TV Technologies], ITunerCap interface [Microsoft TV Technologies],described, ITunerCapInterface, mstv.itunercap, tuner/ITunerCap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITunerCap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITunerCap interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>ITunerCap</b> interface provides information about the capabilities of a BDA device filter that represents a TV tuner.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITunerCap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITunerCap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITunerCap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a885d849-e6d8-477a-a629-1c1a6152bc9b">get_AuxInputCount</a>
</td>
<td align="left" width="63%">
Retrieves a count of the number of auxiliary inputs on the TV tuner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9763a977-c19a-4e6e-bcd6-93dabd357fbe">get_SupportedNetworkTypes</a>
</td>
<td align="left" width="63%">
Retrieves a list of the network types that are supported by the TV tuner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/301402bd-8c9c-4dab-a00b-29aaa8efb2a2">get_SupportedVideoFormats</a>
</td>
<td align="left" width="63%">
Retrieves the video formats that are supported by the TV tuner.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITunerCap)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

