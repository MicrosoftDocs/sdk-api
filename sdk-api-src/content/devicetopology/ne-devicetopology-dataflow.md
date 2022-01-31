---
UID: NE:devicetopology.__MIDL___MIDL_itf_devicetopology_0000_0000_0011
title: DataFlow (devicetopology.h)
description: The DataFlow enumeration indicates the data-flow direction of an audio stream through a connector.
helpviewer_keywords: ["DataFlow","DataFlow","DataFlow enumeration [Core Audio]","In","Out","coreaudio.dataflow","devicetopology/DataFlow","devicetopology/In","devicetopology/Out"]
old-location: coreaudio\dataflow.htm
tech.root: CoreAudio
ms.assetid: bdc2336c-5609-43f2-9b65-d8806f0fc63b
ms.date: 12/05/2018
ms.keywords: DataFlow, DataFlow , DataFlow enumeration [Core Audio], In, Out, coreaudio.dataflow, devicetopology/DataFlow, devicetopology/In, devicetopology/Out
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
targetos: Windows
req.typenames: DataFlow
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_devicetopology_0000_0000_0011
 - devicetopology/__MIDL___MIDL_itf_devicetopology_0000_0000_0011
 - DataFlow
 - devicetopology/DataFlow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Devicetopology.h
api_name:
 - DataFlow
---

# DataFlow enumeration


## -description

The <b>DataFlow</b> enumeration indicates the data-flow direction of an audio stream through a connector.

## -enum-fields

### -field In:0

Input stream. The audio stream flows into the device through the connector.

### -field Out

Output stream. The audio stream flows out of the device through the connector.

## -remarks

The <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getdataflow">IConnector::GetDataFlow</a> method uses the constants defined in the <b>DataFlow</b> enumeration.

The topology of a rendering or capture device on an audio adapter typically has one or more connectors with a data-flow direction of "In" through which audio data enters the device, and one or more connectors with a data-flow direction of "Out" through which audio data exits the device. For example, a typical rendering device on an adapter has a connector with data-flow direction "In" through which the Windows audio engine streams PCM data into the device. The same device has a connector with data-flow direction "Out" through which the device transmits an audio signal to speakers or headphones.

The topology of a rendering endpoint device (for example, headphones) has a single connector with data-flow direction "In" through which audio data (in the form of an analog signal) enters the device.

The topology of a capture endpoint device (for example, a microphone) has a single connector with data-flow direction "Out" through which audio data exits the device.

For more information, see <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-constants">Core Audio Constants</a>



<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getdataflow">IConnector::GetDataFlow</a>
