---
UID: NN:devicetopology.ISubunit
title: ISubunit
author: windows-sdk-content
description: The ISubunit interface represents a hardware subunit (for example, a volume control) that lies in the data path between a client and an audio endpoint device.
old-location: coreaudio\isubunit.htm
tech.root: CoreAudio
ms.assetid: 9ec630bc-bba1-4a44-b66d-404a5221abbf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ISubunit, ISubunit interface [Core Audio], ISubunit interface [Core Audio],described, coreaudio.isubunit, devicetopology/ISubunit
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# ISubunit interface


## -description



The <b>ISubunit</b> interface represents a hardware subunit (for example, a volume control) that lies in the data path between a client and an audio endpoint device. The client obtains a reference to an <b>ISubunit</b> interface by calling the <a href="https://msdn.microsoft.com/6251cabd-9284-4311-bd5c-0c5b6d9a9be4">IDeviceTopology::GetSubunit</a> method, or by calling the <b>IPart::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_ISubunit.




## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/6251cabd-9284-4311-bd5c-0c5b6d9a9be4">IDeviceTopology::GetSubunit</a>



<a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart Interface</a>
 

 

