---
UID: NN:devicetopology.IKsFormatSupport
title: IKsFormatSupport (devicetopology.h)
description: The IKsFormatSupport interface provides information about the audio data formats that are supported by a software-configured I/O connection (typically a DMA channel) between an audio adapter device and system memory.
helpviewer_keywords: ["IKsFormatSupport","IKsFormatSupport interface [Core Audio]","IKsFormatSupport interface [Core Audio]","described","coreaudio.iksformatsupport","devicetopology/IKsFormatSupport"]
old-location: coreaudio\iksformatsupport.htm
tech.root: CoreAudio
ms.assetid: 53a29b57-1650-4e4d-b9d2-95307063a733
ms.date: 12/05/2018
ms.keywords: IKsFormatSupport, IKsFormatSupport interface [Core Audio], IKsFormatSupport interface [Core Audio],described, coreaudio.iksformatsupport, devicetopology/IKsFormatSupport
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
 - IKsFormatSupport
 - devicetopology/IKsFormatSupport
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
 - IKsFormatSupport
---

# IKsFormatSupport interface


## -description

The <b>IKsFormatSupport</b> interface provides information about the audio data formats that are supported by a software-configured I/O connection (typically a DMA channel) between an audio adapter device and system memory. The client obtains a reference to the <b>IKsFormatSupport</b> interface of a part by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to REFIID IID_IKsFormatSupport. The call to <b>IPart::Activate</b> succeeds only if the part supports the <b>IKsFormatSupport</b> interface. Only a part object that represents a connector with a Software_IO connection type will support this interface. For more information about Software_IO, see <a href="/windows/win32/api/devicetopology/ne-devicetopology-connectortype">ConnectorType Enumeration</a>.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsFormatSupport</b> interface provides convenient access to the KSPROPERTY_PIN_DATAINTERSECTION and KSPROPERTY_PIN_PROPOSEDDATAFORMAT properties of a connector to a system bus (typically, PCI or PCI Express) or an external bus (for example, USB). Not all drivers support the KSPROPERTY_PIN_PROPOSEDDATAFORMAT property. If a driver does not support this property, <b>IKsFormatSupport</b> uses the information in the KS data ranges for the connector to determine whether the connector supports the proposed format. For more information about KS properties, KS pins, and KS data ranges, see the Windows DDK documentation.

## -inheritance

The <b>IKsFormatSupport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsFormatSupport</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
