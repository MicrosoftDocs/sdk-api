---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITLegacyWaveSupport interface


## -description


The 
<b>ITLegacyWaveSupport</b> interface allows an application to discover whether a terminal created by a legacy TSP (pre-TAPI 3) can be controlled using the  Wave API.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyWaveSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITLegacyWaveSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLegacyWaveSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/117586d7-8214-4fc8-9c7d-08865582cc2a">IsFullDuplex</a>
</td>
<td align="left" width="63%">
Gets indicator of whether address supports wave devices.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/36f9f126-361f-448a-a464-ffef1de25d26">FULLDUPLEX_SUPPORT</a>
 

 

