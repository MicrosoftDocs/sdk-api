---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA structure


## -description


Represents key exchange output data for hardware content protection.


## -struct-fields




### -field PrivateDataSize

The size of the private data reserved for IHV usage. This size is determined from the <i>pPrivateOutputSize</i> parameter returned by the <a href="https://msdn.microsoft.com/3F973DA0-F722-4EC2-A578-F01B6999F16B">ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize</a> function.


### -field MaxHWProtectionDataSize

The maximum size of data that the driver can return in the output buffer. The last byte that it can write to is <b>pbOuput</b>[<b>PrivateDataSize</b> + <b>MaxHWProtectionDataSize</b> – 1].


### -field HWProtectionDataSize

The size of the output data written by the driver.


### -field TransportTime

The number of 100 nanosecond units spent transporting the data.


### -field ExecutionTime

The number of 100 nanosecond units spent executing the content protection command.


### -field pbOutput

If <b>PrivateDataSize</b> is greater than 0,  pbInput[0] – <b>pbOutput</b>[<b>PrivateDataSize</b> - 1] is reserved for IHV use.

<b>pbOutput</b>[<b>PrivateDataSize</b>] – <b>pbOutput</b>[<b>HWProtectionDataSize</b> + <b>PrivateDataSize</b> - 1] contains the input data for the DRM command. The format and size of the DRM command is defined by the DRM specification.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

