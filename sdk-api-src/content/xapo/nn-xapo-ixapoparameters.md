---
UID: NN:xapo.IXAPOParameters
title: IXAPOParameters
author: windows-sdk-content
description: An optional interface that allows an XAPO to use effect-specific parameters.
old-location: xaudio2\ixapoparameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixapoparameters.IXAPOParameters
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IXAPOParameters, IXAPOParameters interface [XAudio2 Audio Mixing APIs], IXAPOParameters interface [XAudio2 Audio Mixing APIs],described, xapo/IXAPOParameters, xaudio2.ixapoparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAPOParameters interface


## -description


An optional interface that allows an XAPO to use effect-specific parameters.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAPOParameters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXAPOParameters</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/FBF27BCD-6B20-4D8A-BD9D-8E0889889F8B">GetParameters</a>
</td>
<td align="left" width="63%">
Gets the current values for any effect-specific parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">SetParameters</a>
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




<a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">Interfaces</a>
 

 

