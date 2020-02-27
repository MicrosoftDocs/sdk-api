---
UID: NN:xapo.IXAPOParameters
title: IXAPOParameters (xapo.h)
description: An optional interface that allows an XAPO to use effect-specific parameters.
old-location: xaudio2\ixapoparameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixapoparameters.IXAPOParameters
ms.date: 12/05/2018
ms.keywords: IXAPOParameters, IXAPOParameters interface [XAudio2 Audio Mixing APIs], IXAPOParameters interface [XAudio2 Audio Mixing APIs],described, xapo/IXAPOParameters, xaudio2.ixapoparameters
f1_keywords:
- xapo/IXAPOParameters
dev_langs:
- c++
req.header: xapo.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- XAPO.h
api_name:
- IXAPOParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXAPOParameters interface


## -description


An optional interface that allows an XAPO to use effect-specific parameters.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAPOParameters</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXAPOParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXAPOParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xapo/nf-xapo-ixapoparameters-getparameters">GetParameters</a>
</td>
<td align="left" width="63%">
Gets the current values for any effect-specific parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">SetParameters</a>
</td>
<td align="left" width="63%">
Sets effect-specific parameters.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/xaudio2/interfaces">Interfaces</a>
 

 

