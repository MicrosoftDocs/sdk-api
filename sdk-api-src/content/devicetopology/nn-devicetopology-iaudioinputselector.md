---
UID: NN:devicetopology.IAudioInputSelector
title: IAudioInputSelector (devicetopology.h)
description: The IAudioInputSelector interface provides access to a hardware multiplexer control (input selector).
helpviewer_keywords: ["IAudioInputSelector","IAudioInputSelector interface [Core Audio]","IAudioInputSelector interface [Core Audio]","described","coreaudio.iaudioinputselector","devicetopology/IAudioInputSelector"]
old-location: coreaudio\iaudioinputselector.htm
tech.root: CoreAudio
ms.assetid: 6f5ce9c0-39e4-4fab-910c-9a11b90fcde7
ms.date: 12/05/2018
ms.keywords: IAudioInputSelector, IAudioInputSelector interface [Core Audio], IAudioInputSelector interface [Core Audio],described, coreaudio.iaudioinputselector, devicetopology/IAudioInputSelector
f1_keywords:
- devicetopology/IAudioInputSelector
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
- IAudioInputSelector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioInputSelector interface


## -description



The <b>IAudioInputSelector</b> interface provides access to a hardware multiplexer control (input selector). The client obtains a reference to the <b>IAudioInputSelector</b> interface of a subunit by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioInputSelector. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioInputSelector</b> interface. Only a subunit object that represents a hardware input selector will support this interface.

Each input of an input selector is identified by the local ID of the part (a connector or subunit of a device topology) that has a direct link to the input. A local ID is a number that uniquely identifies a part among all the parts in a device topology.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioInputSelector</b> interface provides convenient access to the KSPROPERTY_AUDIO_MUX_SOURCE property of a subunit that has a subtype GUID value of KSNODETYPE_MUX. To obtain the subtype GUID of a subunit, call the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

For a code example that uses the <b>IAudioInputSelector</b> interface, see the implementation of the SelectCaptureDevice function in <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioInputSelector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioInputSelector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioInputSelector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the local ID of the part that is connected to the selector input that is currently selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iaudioinputselector-setselection">SetSelection</a>
</td>
<td align="left" width="63%">
Selects one of the inputs of the input selector.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
 

 

