---
UID: NN:devicetopology.IPartsList
title: IPartsList (devicetopology.h)
description: The IPartsList interface represents a list of parts, each of which is an object with an IPart interface that represents a connector or subunit.
helpviewer_keywords: ["IPartsList","IPartsList interface [Core Audio]","IPartsList interface [Core Audio]","described","coreaudio.ipartslist","devicetopology/IPartsList"]
old-location: coreaudio\ipartslist.htm
tech.root: CoreAudio
ms.assetid: 3ac48781-90c2-4b23-aa68-3453091bde61
ms.date: 12/05/2018
ms.keywords: IPartsList, IPartsList interface [Core Audio], IPartsList interface [Core Audio],described, coreaudio.ipartslist, devicetopology/IPartsList
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
 - IPartsList
 - devicetopology/IPartsList
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
 - IPartsList
---

# IPartsList interface


## -description

The <b>IPartsList</b> interface represents a list of parts, each of which is an object with an <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface that represents a connector or subunit. A client obtains a reference to an <b>IPartsList</b> interface by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsincoming">IPart::EnumPartsIncoming</a>, <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsoutgoing">IPart::EnumPartsOutgoing</a>, or <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsignalpath">IDeviceTopology::GetSignalPath</a> method.

For a code example that uses the <b>IPartsList</b> interface, see the implementation of the SelectCaptureDevice function in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -inheritance

The <b>IPartsList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPartsList</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsignalpath">IDeviceTopology::GetSignalPath</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsincoming">IPart::EnumPartsIncoming</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-enumpartsoutgoing">IPart::EnumPartsOutgoing</a>
