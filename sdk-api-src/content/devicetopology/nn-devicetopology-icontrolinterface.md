---
UID: NN:devicetopology.IControlInterface
title: IControlInterface (devicetopology.h)
description: The IControlInterface interface represents a control interface on a part (connector or subunit) in a device topology. The client obtains a reference to a part's IControlInterface interface by calling the IPart::GetControlInterface method.
helpviewer_keywords: ["IControlInterface","IControlInterface interface [Core Audio]","IControlInterface interface [Core Audio]","described","coreaudio.icontrolinterface","devicetopology/IControlInterface"]
old-location: coreaudio\icontrolinterface.htm
tech.root: CoreAudio
ms.assetid: fdd91f65-e45c-4f14-a55c-a44be1661950
ms.date: 12/05/2018
ms.keywords: IControlInterface, IControlInterface interface [Core Audio], IControlInterface interface [Core Audio],described, coreaudio.icontrolinterface, devicetopology/IControlInterface
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
 - IControlInterface
 - devicetopology/IControlInterface
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
 - IControlInterface
---

# IControlInterface interface


## -description

The <b>IControlInterface</b> interface represents a control interface on a part (connector or subunit) in a <a href="/windows/desktop/CoreAudio/device-topologies">device topology</a>. The client obtains a reference to a part's <b>IControlInterface</b> interface by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getcontrolinterface">IPart::GetControlInterface</a> method.

## -inheritance

The <b>IControlInterface</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IControlInterface</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getcontrolinterface">IPart::GetControlInterface</a>
