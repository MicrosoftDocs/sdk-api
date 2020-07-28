---
UID: NN:devicetopology.IKsJackSinkInformation
title: IKsJackSinkInformation (devicetopology.h)
description: The IKsJackSinkInformation interface provides access to jack sink information if the jack is supported by the hardware.
helpviewer_keywords: ["IKsJackSinkInformation","IKsJackSinkInformation interface [Core Audio]","IKsJackSinkInformation interface [Core Audio]","described","coreaudio.iksjacksinkinformation","devicetopology/IKsJackSinkInformation"]
old-location: coreaudio\iksjacksinkinformation.htm
tech.root: CoreAudio
ms.assetid: 4116a912-5ff2-4fc0-96c6-61d1e62cd973
ms.date: 12/05/2018
ms.keywords: IKsJackSinkInformation, IKsJackSinkInformation interface [Core Audio], IKsJackSinkInformation interface [Core Audio],described, coreaudio.iksjacksinkinformation, devicetopology/IKsJackSinkInformation
f1_keywords:
- devicetopology/IKsJackSinkInformation
dev_langs:
- c++
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- IKsJackSinkInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IKsJackSinkInformation interface


## -description


The <b>IKsJackSinkInformation</b> interface provides access to jack sink information if the jack is supported by the hardware.

The client obtains a reference to the <b>IKsJackSinkInformation</b> interface by activating it on the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface of a bridge pin connector on a KS filter device topology object. To activate the object, call the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter refiid set to REFIID <b>IID_IKsJackSinkInformation</b>. 

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsJackSinkInformation</b> interface provides convenient access to the <b>KSPROPERTY_JACK_SINK_INFO</b> property of a connector to an endpoint device. For more information about KS properties and KS pins, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsJackSinkInformation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsJackSinkInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKsJackSinkInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation">GetJackSinkInformation</a>
</td>
<td align="left" width="63%">
Retrieves the sink information for the specified jack. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-iksjackdescription">IKsJackDescription</a>
 

 

