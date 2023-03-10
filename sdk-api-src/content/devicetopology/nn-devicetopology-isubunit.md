---
UID: NN:devicetopology.ISubunit
title: ISubunit (devicetopology.h)
description: The ISubunit interface represents a hardware subunit (for example, a volume control) that lies in the data path between a client and an audio endpoint device.
helpviewer_keywords: ["ISubunit","ISubunit interface [Core Audio]","ISubunit interface [Core Audio]","described","coreaudio.isubunit","devicetopology/ISubunit"]
old-location: coreaudio\isubunit.htm
tech.root: CoreAudio
ms.assetid: 9ec630bc-bba1-4a44-b66d-404a5221abbf
ms.date: 12/05/2018
ms.keywords: ISubunit, ISubunit interface [Core Audio], ISubunit interface [Core Audio],described, coreaudio.isubunit, devicetopology/ISubunit
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
 - ISubunit
 - devicetopology/ISubunit
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
 - ISubunit
---

# ISubunit interface


## -description

The <b>ISubunit</b> interface represents a hardware subunit (for example, a volume control) that lies in the data path between a client and an audio endpoint device. The client obtains a reference to an <b>ISubunit</b> interface by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunit">IDeviceTopology::GetSubunit</a> method, or by calling the <b>IPart::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_ISubunit.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunit">IDeviceTopology::GetSubunit</a>



<a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>