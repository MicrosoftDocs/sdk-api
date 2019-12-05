---
UID: NN:devicetopology.IAudioOutputSelector
title: IAudioOutputSelector (devicetopology.h)
description: The IAudioOutputSelector interface provides access to a hardware demultiplexer control (output selector).
old-location: coreaudio\iaudiooutputselector.htm
tech.root: CoreAudio
ms.assetid: 571a44b6-972f-4d75-a31f-0e02cf728764
ms.date: 12/05/2018
ms.keywords: IAudioOutputSelector, IAudioOutputSelector interface [Core Audio], IAudioOutputSelector interface [Core Audio],described, coreaudio.iaudiooutputselector, devicetopology/IAudioOutputSelector
ms.topic: interface
f1_keywords:
- devicetopology/IAudioOutputSelector
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
- IAudioOutputSelector
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioOutputSelector interface


## -description



The <b>IAudioOutputSelector</b> interface provides access to a hardware demultiplexer control (output selector). The client obtains a reference to the <b>IAudioOutputSelector</b> interface of a subunit by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioOutputSelector. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioOutputSelector</b> interface. Only a subunit object that represents a hardware output selector will support this interface.

Each output of an output selector is identified by the local ID of the part (a connector or subunit of a device topology) with a direct link to the output. A local ID is a number that uniquely identifies a part among all the parts in a device topology.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioOutputSelector</b> interface provides convenient access to the KSPROPERTY_AUDIO_DEMUX_DEST property of a subunit that has a subtype GUID value of KSNODETYPE_DEMUX. To obtain the subtype GUID of a subunit, call the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioOutputSelector</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioOutputSelector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioOutputSelector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the local ID of the part that is connected to the selector output that is currently selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-iaudiooutputselector-setselection">SetSelection</a>
</td>
<td align="left" width="63%">
Selects one of the outputs of the output selector.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
 

 

