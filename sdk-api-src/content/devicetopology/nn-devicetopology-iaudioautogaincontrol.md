---
UID: NN:devicetopology.IAudioAutoGainControl
title: IAudioAutoGainControl (devicetopology.h)
description: The IAudioAutoGainControl interface provides access to a hardware automatic gain control (AGC).
helpviewer_keywords: ["IAudioAutoGainControl","IAudioAutoGainControl interface [Core Audio]","IAudioAutoGainControl interface [Core Audio]","described","coreaudio.iaudioautogaincontrol","devicetopology/IAudioAutoGainControl"]
old-location: coreaudio\iaudioautogaincontrol.htm
tech.root: CoreAudio
ms.assetid: f21e27e6-f3a0-418a-ad2e-e3e104dd6da2
ms.date: 12/05/2018
ms.keywords: IAudioAutoGainControl, IAudioAutoGainControl interface [Core Audio], IAudioAutoGainControl interface [Core Audio],described, coreaudio.iaudioautogaincontrol, devicetopology/IAudioAutoGainControl
f1_keywords:
- devicetopology/IAudioAutoGainControl
dev_langs:
- c++
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- Devicetopology.h
api_name:
- IAudioAutoGainControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioAutoGainControl interface


## -description



The <b>IAudioAutoGainControl</b> interface provides access to a hardware automatic gain control (AGC). The client obtains a reference to the <b>IAudioAutoGainControl</b> interface of a subunit by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioAutoGainControl. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioAutoGainControl</b> interface. Only a subunit object that represents a hardware AGC function will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioAutoGainControl</b> interface provides convenient access to the KSPROPERTY_AUDIO_AGC property of a subunit that has a subtype GUID value of KSNODETYPE_AGC. To obtain the subtype GUID of a subunit, call the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioAutoGainControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioAutoGainControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioAutoGainControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iaudioautogaincontrol-getenabled">GetEnabled</a>
</td>
<td align="left" width="63%">
Gets the current state (enabled or disabled) of the AGC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iaudioautogaincontrol-setenabled">SetEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables the AGC.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
 

 

