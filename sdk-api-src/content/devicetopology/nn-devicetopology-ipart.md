---
UID: NN:devicetopology.IPart
title: IPart (devicetopology.h)
description: The IPart interface represents a part (connector or subunit) of a device topology.
helpviewer_keywords: ["IPart","IPart interface [Core Audio]","IPart interface [Core Audio]","described","coreaudio.ipart","devicetopology/IPart"]
old-location: coreaudio\ipart.htm
tech.root: CoreAudio
ms.assetid: 3bcfab9f-fad8-4605-8780-0b7c2068fcdf
ms.date: 12/05/2018
ms.keywords: IPart, IPart interface [Core Audio], IPart interface [Core Audio],described, coreaudio.ipart, devicetopology/IPart
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
 - IPart
 - devicetopology/IPart
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
 - IPart
---

# IPart interface


## -description

The <b>IPart</b> interface represents a part (connector or subunit) of a device topology. A client obtains a reference to an <b>IPart</b> interface by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a> or <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getpart">IPartsList::GetPart</a> method, or by calling the <b>QueryInterface</b> method of the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> or <a href="/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit</a> interface on a part object and setting the method's <i>iid</i> parameter to <b>REFIID</b> IID_IPart.

An object with an <b>IPart</b> interface can encapsulate one of the following device topology parts:

<ul>
<li><b>Connector.</b> This is a part that connects to another device to form a data path for transmitting an audio stream between devices.</li>
<li><b>Subunit.</b> This is a part that processes an audio stream (for example, volume control).</li>
</ul>
The <b>IPart</b> interface of a connector or subunit object represents the generic functions that are common to all parts, and the object's <b>IConnector</b> or <b>ISubunit</b> interface represents the functions that are specific to a connector or subunit. In addition, a part might support one or more control interfaces for controlling or monitoring the function of the part. For example, the client controls a volume-control subunit through its <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel</a> interface.

The <b>IPart</b> interface provides methods for getting the name, local ID, global ID, and part type of a connector or subunit. In addition, <b>IPart</b> can activate a control interface on a connector or subunit.

For code examples that use the <b>IPart</b> interface, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -inheritance

The <b>IPart</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPart</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiovolumelevel">IAudioVolumeLevel Interface</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getpartbyid">IDeviceTopology::GetPartById</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipartslist-getpart">IPartsList::GetPart</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-isubunit">ISubunit Interface</a>
