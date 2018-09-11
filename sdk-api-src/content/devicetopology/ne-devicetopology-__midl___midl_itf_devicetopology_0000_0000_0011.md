---
UID: NE:devicetopology.__MIDL___MIDL_itf_devicetopology_0000_0000_0011
title: "__MIDL___MIDL_itf_devicetopology_0000_0000_0011"
author: windows-sdk-content
description: The DataFlow enumeration indicates the data-flow direction of an audio stream through a connector.
old-location: coreaudio\dataflow.htm
tech.root: CoreAudio
ms.assetid: bdc2336c-5609-43f2-9b65-d8806f0fc63b
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: DataFlow, DataFlow , DataFlow enumeration [Core Audio], In, Out, __MIDL___MIDL_itf_devicetopology_0000_0000_0011, coreaudio.dataflow, devicetopology/DataFlow, devicetopology/In, devicetopology/Out
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - DataFlow
product: Windows
targetos: Windows
req.typenames: DataFlow
req.redist: 
---

# __MIDL___MIDL_itf_devicetopology_0000_0000_0011 enumeration


## -description



The <b>DataFlow</b> enumeration indicates the data-flow direction of an audio stream through a connector.




## -enum-fields




### -field In

Input stream. The audio stream flows into the device through the connector.


### -field Out

Output stream. The audio stream flows out of the device through the connector.


## -remarks



The <a href="https://msdn.microsoft.com/55078775-2921-45c2-af27-c8ad53688293">IConnector::GetDataFlow</a> method uses the constants defined in the <b>DataFlow</b> enumeration.

The topology of a rendering or capture device on an audio adapter typically has one or more connectors with a data-flow direction of "In" through which audio data enters the device, and one or more connectors with a data-flow direction of "Out" through which audio data exits the device. For example, a typical rendering device on an adapter has a connector with data-flow direction "In" through which the Windows audio engine streams PCM data into the device. The same device has a connector with data-flow direction "Out" through which the device transmits an audio signal to speakers or headphones.

The topology of a rendering endpoint device (for example, headphones) has a single connector with data-flow direction "In" through which audio data (in the form of an analog signal) enters the device.

The topology of a capture endpoint device (for example, a microphone) has a single connector with data-flow direction "Out" through which audio data exits the device.

For more information, see <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>.




## -see-also




<a href="https://msdn.microsoft.com/9dc9f182-3adf-4171-8829-35debae123da">Core Audio Constants</a>



<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/55078775-2921-45c2-af27-c8ad53688293">IConnector::GetDataFlow</a>
 

 

