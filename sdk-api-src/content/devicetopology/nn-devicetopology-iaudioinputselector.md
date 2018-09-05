---
UID: NN:devicetopology.IAudioInputSelector
title: IAudioInputSelector
author: windows-sdk-content
description: The IAudioInputSelector interface provides access to a hardware multiplexer control (input selector).
old-location: coreaudio\iaudioinputselector.htm
old-project: CoreAudio
ms.assetid: 6f5ce9c0-39e4-4fab-910c-9a11b90fcde7
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioInputSelector, IAudioInputSelector interface [Core Audio], IAudioInputSelector interface [Core Audio],described, coreaudio.iaudioinputselector, devicetopology/IAudioInputSelector
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: devicetopology.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioInputSelector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioInputSelector interface


## -description



The <b>IAudioInputSelector</b> interface provides access to a hardware multiplexer control (input selector). The client obtains a reference to the <b>IAudioInputSelector</b> interface of a subunit by calling the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IAudioInputSelector. The call to <b>IPart::Activate</b> succeeds only if the subunit supports the <b>IAudioInputSelector</b> interface. Only a subunit object that represents a hardware input selector will support this interface.

Each input of an input selector is identified by the local ID of the part (a connector or subunit of a device topology) that has a direct link to the input. A local ID is a number that uniquely identifies a part among all the parts in a device topology.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IAudioInputSelector</b> interface provides convenient access to the KSPROPERTY_AUDIO_MUX_SOURCE property of a subunit that has a subtype GUID value of KSNODETYPE_MUX. To obtain the subtype GUID of a subunit, call the <a href="https://msdn.microsoft.com/456aaafb-1e68-4a3a-b27b-c6f6f89dc17b">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

For a code example that uses the <b>IAudioInputSelector</b> interface, see the implementation of the SelectCaptureDevice function in <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioInputSelector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioInputSelector</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/38288a63-62a3-4b06-b2e6-dbe8c27e09ad">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the local ID of the part that is connected to the selector input that is currently selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6291447-d3a9-4bc7-808c-9427e1642752">SetSelection</a>
</td>
<td align="left" width="63%">
Selects one of the inputs of the input selector.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a>
 

 

