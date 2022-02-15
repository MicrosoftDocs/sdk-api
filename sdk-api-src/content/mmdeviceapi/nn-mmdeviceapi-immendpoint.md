---
UID: NN:mmdeviceapi.IMMEndpoint
title: IMMEndpoint (mmdeviceapi.h)
description: The IMMEndpoint interface represents an audio endpoint device.
helpviewer_keywords: ["IMMEndpoint","IMMEndpoint interface [Core Audio]","IMMEndpoint interface [Core Audio]","described","coreaudio.immendpoint","mmdeviceapi/IMMEndpoint"]
old-location: coreaudio\immendpoint.htm
tech.root: CoreAudio
ms.assetid: 293de8eb-204a-4c18-807c-b1405db85b12
ms.date: 12/05/2018
ms.keywords: IMMEndpoint, IMMEndpoint interface [Core Audio], IMMEndpoint interface [Core Audio],described, coreaudio.immendpoint, mmdeviceapi/IMMEndpoint
req.header: mmdeviceapi.h
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
 - IMMEndpoint
 - mmdeviceapi/IMMEndpoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMEndpoint
---

# IMMEndpoint interface


## -description

The <b>IMMEndpoint</b> interface represents an <a href="/windows/desktop/CoreAudio/audio-endpoint-devices">audio endpoint device</a>. A client obtains a reference to an <b>IMMEndpoint</b> interface instance by following these steps:

<ol>
<li>By using one of the techniques described in <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface of an audio endpoint device.</li>
<li>Call the <b>IMMDevice::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IMMEndpoint.</li>
</ol>

## -inheritance

The <b>IMMEndpoint</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMMEndpoint</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/CoreAudio/mmdevice-api">MMDevice API</a>
