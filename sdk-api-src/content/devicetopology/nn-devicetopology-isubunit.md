---
UID: NN:devicetopology.ISubunit
title: ISubunit (devicetopology.h)
author: windows-sdk-content
description: The ISubunit interface represents a hardware subunit (for example, a volume control) that lies in the data path between a client and an audio endpoint device.
old-location: coreaudio\isubunit.htm
tech.root: CoreAudio
ms.assetid: 9ec630bc-bba1-4a44-b66d-404a5221abbf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISubunit, ISubunit interface [Core Audio], ISubunit interface [Core Audio],described, coreaudio.isubunit, devicetopology/ISubunit
ms.topic: interface
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
 - COM
api_location:
 - Devicetopology.h
api_name:
 - ISubunit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISubunit interface


## -description



The <b>ISubunit</b> interface represents a hardware subunit (for example, a volume control) that lies in the data path between a client and an audio endpoint device. The client obtains a reference to an <b>ISubunit</b> interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunit">IDeviceTopology::GetSubunit</a> method, or by calling the <b>IPart::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_ISubunit.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getsubunit">IDeviceTopology::GetSubunit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart Interface</a>
 

 

