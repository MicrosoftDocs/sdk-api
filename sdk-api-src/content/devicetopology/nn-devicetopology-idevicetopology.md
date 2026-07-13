---
UID: NN:devicetopology.IDeviceTopology
title: IDeviceTopology (devicetopology.h)
description: The IDeviceTopology interface provides access to the topology of an audio device.
helpviewer_keywords: ["IDeviceTopology","IDeviceTopology interface [Core Audio]","IDeviceTopology interface [Core Audio]","described","coreaudio.idevicetopology","devicetopology/IDeviceTopology"]
old-location: coreaudio\idevicetopology.htm
tech.root: CoreAudio
ms.assetid: 1b509f69-6277-40c0-a293-02afc30d464a
ms.date: 12/05/2018
ms.keywords: IDeviceTopology, IDeviceTopology interface [Core Audio], IDeviceTopology interface [Core Audio],described, coreaudio.idevicetopology, devicetopology/IDeviceTopology
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeviceTopology
 - devicetopology/IDeviceTopology
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IDeviceTopology
---

# IDeviceTopology interface


## -description

The <b>IDeviceTopology</b> interface provides access to the topology of an audio device. The topology of an audio <i>adapter</i> device consists of the data paths that lead to and from audio endpoint devices and the control points that lie along the paths. An audio <i>endpoint</i> device also has a topology, but it is trivial, as explained in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>. A client obtains a reference to the <b>IDeviceTopology</b> interface for an audio endpoint device by following these steps:

<ol>
<li>By using one of the techniques described in <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface for an audio endpoint device.</li>
<li>Call the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b> IID_IDeviceTopology.</li>
</ol>
After obtaining the <b>IDeviceTopology</b> interface for an audio endpoint device, an application can explore the topologies of the audio adapter devices to which the endpoint device is connected.

For code examples that use the <b>IDeviceTopology</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -inheritance

The <b>IDeviceTopology</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeviceTopology</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>
