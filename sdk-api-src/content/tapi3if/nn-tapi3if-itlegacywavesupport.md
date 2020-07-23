---
UID: NN:tapi3if.ITLegacyWaveSupport
title: ITLegacyWaveSupport (tapi3if.h)
description: The ITLegacyWaveSupport interface allows an application to discover whether a terminal created by a legacy TSP (pre-TAPI 3) can be controlled using the Wave API.
helpviewer_keywords: ["ITLegacyWaveSupport","ITLegacyWaveSupport interface [TAPI 2.2]","ITLegacyWaveSupport interface [TAPI 2.2]","described","_tapi3_itlegacywavesupport","tapi3.itlegacywavesupport","tapi3if/ITLegacyWaveSupport"]
old-location: tapi3\itlegacywavesupport.htm
tech.root: tapi3
ms.assetid: f1ef5f5d-822d-466d-997e-e9c1a09abcbe
ms.date: 12/05/2018
ms.keywords: ITLegacyWaveSupport, ITLegacyWaveSupport interface [TAPI 2.2], ITLegacyWaveSupport interface [TAPI 2.2],described, _tapi3_itlegacywavesupport, tapi3.itlegacywavesupport, tapi3if/ITLegacyWaveSupport
f1_keywords:
- tapi3if/ITLegacyWaveSupport
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITLegacyWaveSupport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITLegacyWaveSupport interface


## -description


The 
<b>ITLegacyWaveSupport</b> interface allows an application to discover whether a terminal created by a legacy TSP (pre-TAPI 3) can be controlled using the  Wave API.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyWaveSupport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITLegacyWaveSupport</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacywavesupport-isfullduplex">IsFullDuplex</a>
</td>
<td align="left" width="63%">
Gets indicator of whether address supports wave devices.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-fullduplex_support">FULLDUPLEX_SUPPORT</a>
 

 

