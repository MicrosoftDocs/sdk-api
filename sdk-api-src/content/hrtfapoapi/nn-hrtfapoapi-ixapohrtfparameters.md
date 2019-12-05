---
UID: NN:hrtfapoapi.IXAPOHrtfParameters
title: IXAPOHrtfParameters (hrtfapoapi.h)
description: The interface used to set parameters that control how head-related transfer function (HRTF) is applied to a sound.
old-location: xaudio2\ixapohrtfparameters.htm
tech.root: xaudio2
ms.assetid: EDA29173-84B5-4D2F-90B0-546EEEC49539
ms.date: 12/05/2018
ms.keywords: IXAPOHrtfParameters, IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs], IXAPOHrtfParameters interface [XAudio2 Audio Mixing APIs],described, hrtfapoapi/IXAPOHrtfParameters, xaudio2.ixapohrtfparameters
ms.topic: interface
f1_keywords:
- hrtfapoapi/IXAPOHrtfParameters
dev_langs:
- c++
req.header: hrtfapoapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: HrtfApo.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- HrtfApo.dll
api_name:
- IXAPOHrtfParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXAPOHrtfParameters interface


## -description


The interface used to set parameters that control how head-related transfer function (HRTF) is applied to a sound.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAPOHrtfParameters</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXAPOHrtfParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXAPOHrtfParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/hrtfapoapi/nf-hrtfapoapi-ixapohrtfparameters-setenvironment">SetEnvironment</a>
</td>
<td align="left" width="63%">
Selects the acoustic environment to simulate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/hrtfapoapi/nf-hrtfapoapi-ixapohrtfparameters-setsourcegain">SetSourceGain</a>
</td>
<td align="left" width="63%">
Sets the custom direct-path gain value for the current source position. Valid only for sounds played with the HrtfDistanceDecayType custom decay type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/hrtfapoapi/nf-hrtfapoapi-ixapohrtfparameters-setsourceorientation">SetSourceOrientation</a>
</td>
<td align="left" width="63%">
Set the rotation matrix for the source orientation, with respect to the listener's coordinate system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/hrtfapoapi/nf-hrtfapoapi-ixapohrtfparameters-setsourceposition">SetSourcePosition</a>
</td>
<td align="left" width="63%">
Sets the position of the sound relative to the listener.

</td>
</tr>
</table> 


## -remarks



Create instances of the XAPO interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/hrtfapoapi/nf-hrtfapoapi-createhrtfapo">CreateHrtfApo</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/xaudio2/interfaces">Interfaces</a>
 

 

