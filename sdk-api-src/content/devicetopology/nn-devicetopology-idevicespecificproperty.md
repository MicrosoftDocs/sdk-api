---
UID: NN:devicetopology.IDeviceSpecificProperty
title: IDeviceSpecificProperty (devicetopology.h)
description: The IDeviceSpecificProperty interface provides access to the control value of a device-specific hardware control.
helpviewer_keywords: ["IDeviceSpecificProperty","IDeviceSpecificProperty interface [Core Audio]","IDeviceSpecificProperty interface [Core Audio]","described","coreaudio.idevicespecificproperty","devicetopology/IDeviceSpecificProperty"]
old-location: coreaudio\idevicespecificproperty.htm
tech.root: CoreAudio
ms.assetid: 52873fe2-7f59-4a30-b526-cbefa27a81bb
ms.date: 12/05/2018
ms.keywords: IDeviceSpecificProperty, IDeviceSpecificProperty interface [Core Audio], IDeviceSpecificProperty interface [Core Audio],described, coreaudio.idevicespecificproperty, devicetopology/IDeviceSpecificProperty
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
 - IDeviceSpecificProperty
 - devicetopology/IDeviceSpecificProperty
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
 - IDeviceSpecificProperty
---

# IDeviceSpecificProperty interface


## -description

The <b>IDeviceSpecificProperty</b> interface provides access to the control value of a device-specific hardware control. A client obtains a reference to an <b>IDeviceSpecificProperty</b> interface of a part by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b> IID_IDeviceSpecificProperty. The call to <b>IPart::Activate</b> succeeds only if the part supports the <b>IDeviceSpecificProperty</b> interface. A part supports this interface only if the underlying hardware control has a device-specific control value and the control cannot be adequately represented by any other interface in the DeviceTopology API.

Typically, a device-specific property is useful only to a client that can infer the meaning of the property value from information such as the part type, part subtype, and part name. The client can obtain this information by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getparttype">IPart::GetPartType</a>, <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a>, and <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getname">IPart::GetName</a> methods.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware control parameters in subunits (referred to as KS nodes). The <b>IDeviceSpecificProperty</b> interface provides convenient access to the KSPROPERTY_AUDIO_DEV_SPECIFIC property of a subunit that has a subtype GUID value of KSNODETYPE_DEV_SPECIFIC. To obtain the subtype GUID of a subunit, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a> method. For more information about KS properties and KS node types, see the Windows DDK documentation.

## -inheritance

The <b>IDeviceSpecificProperty</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeviceSpecificProperty</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getname">IPart::GetName</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getparttype">IPart::GetPartType</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-getsubtype">IPart::GetSubType</a>
