---
UID: NN:devicetopology.IKsJackSinkInformation
title: IKsJackSinkInformation
author: windows-sdk-content
description: The IKsJackSinkInformation interface provides access to jack sink information if the jack is supported by the hardware.
old-location: coreaudio\iksjacksinkinformation.htm
old-project: CoreAudio
ms.assetid: 4116a912-5ff2-4fc0-96c6-61d1e62cd973
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IKsJackSinkInformation, IKsJackSinkInformation interface [Core Audio], IKsJackSinkInformation interface [Core Audio],described, coreaudio.iksjacksinkinformation, devicetopology/IKsJackSinkInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IKsJackSinkInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IKsJackSinkInformation interface


## -description


The <b>IKsJackSinkInformation</b> interface provides access to jack sink information if the jack is supported by the hardware.

The client obtains a reference to the <b>IKsJackSinkInformation</b> interface by activating it on the <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> interface of a bridge pin connector on a KS filter device topology object. To activate the object, call the <a href="https://msdn.microsoft.com/72e08a30-65c0-437b-9932-110ba48a2376">IPart::Activate</a> method with parameter refiid set to REFIID <b>IID_IKsJackSinkInformation</b>. 

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsJackSinkInformation</b> interface provides convenient access to the <b>KSPROPERTY_JACK_SINK_INFO</b> property of a connector to an endpoint device. For more information about KS properties and KS pins, see the Windows DDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsJackSinkInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKsJackSinkInformation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ca4165ce-433a-4a8f-9853-bbe812de90ca">GetJackSinkInformation</a>
</td>
<td align="left" width="63%">
Retrieves the sink information for the specified jack. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/0ca9e719-7179-4302-99ff-df137141f58f">IKsJackDescription</a>
 

 

