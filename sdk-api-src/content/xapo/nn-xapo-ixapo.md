---
UID: NN:xapo.IXAPO
title: IXAPO (xapo.h)
description: The interface for an Audio Processing Object which be used in an XAudio2 effect chain.
helpviewer_keywords: ["IXAPO","IXAPO interface [XAudio2 Audio Mixing APIs]","IXAPO interface [XAudio2 Audio Mixing APIs]","described","xapo/IXAPO","xaudio2.ixapo"]
old-location: xaudio2\ixapo.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixapo.IXAPO
ms.date: 12/05/2018
ms.keywords: IXAPO, IXAPO interface [XAudio2 Audio Mixing APIs], IXAPO interface [XAudio2 Audio Mixing APIs],described, xapo/IXAPO, xaudio2.ixapo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAPO
 - xapo/IXAPO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO
---

# IXAPO interface


## -description

The interface for an Audio Processing Object which be used in an XAudio2 effect chain.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAPO</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXAPO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXAPO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-calcinputframes">CalcInputFrames</a>
</td>
<td align="left" width="63%">
Returns the number of input frames required to generate the given number of output frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-calcoutputframes">CalcOutputFrames</a>
</td>
<td align="left" width="63%">
Returns the number of output frames that will be generated from a given number of input frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-getregistrationproperties">GetRegistrationProperties</a>
</td>
<td align="left" width="63%">
Returns the registration properties of an XAPO. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Performs any effect-specific initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-isinputformatsupported">IsInputFormatSupported</a>
</td>
<td align="left" width="63%">
Queries if a specific input format is supported for a given output format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-isoutputformatsupported">IsOutputFormatSupported</a>
</td>
<td align="left" width="63%">
Queries if a specific output format is supported for a given input format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-lockforprocess">LockForProcess</a>
</td>
<td align="left" width="63%">
Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">Process</a> is called on the realtime thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">Process</a>
</td>
<td align="left" width="63%">
Runs the XAPO's digital signal processing (DSP) code on the given input and output buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets variables dependent on frame history.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-unlockforprocess">UnlockForProcess</a>
</td>
<td align="left" width="63%">
Deallocates variables that were allocated with the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-lockforprocess">LockForProcess</a> method.

</td>
</tr>
</table>

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/interfaces">Interfaces</a>