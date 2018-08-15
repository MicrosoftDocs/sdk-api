---
UID: NN:tapi3if.ITLegacyWaveSupport
title: ITLegacyWaveSupport
author: windows-sdk-content
description: The ITLegacyWaveSupport interface allows an application to discover whether a terminal created by a legacy TSP (pre-TAPI 3) can be controlled using the Wave API.
old-location: tapi3\itlegacywavesupport.htm
old-project: tapi
ms.assetid: f1ef5f5d-822d-466d-997e-e9c1a09abcbe
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITLegacyWaveSupport, ITLegacyWaveSupport interface [TAPI 2.2], ITLegacyWaveSupport interface [TAPI 2.2],described, _tapi3_itlegacywavesupport, tapi3.itlegacywavesupport, tapi3if/ITLegacyWaveSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyWaveSupport
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

