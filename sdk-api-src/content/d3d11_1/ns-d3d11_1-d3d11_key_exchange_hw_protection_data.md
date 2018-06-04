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

# D3D11_KEY_EXCHANGE_HW_PROTECTION_DATA structure


## -description


Represents key exchange data for hardware content protection.


## -struct-fields




### -field HWProtectionFunctionID

The function ID of the DRM command. The values and meanings of the function ID are defined by the DRM specification.


### -field pInputData

Pointer to a buffer containing a <a href="https://msdn.microsoft.com/B3F587BC-0DA8-496B-A3F5-ADFD16ABABB9">D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA</a> structure that specifies memory reserved for IHV use and the input data for the DRM command.


### -field pOutputData

Pointer to a buffer containing a <a href="https://msdn.microsoft.com/D8F987CA-0BD2-42D1-AE95-8D2D118655B1">D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA</a> structure that specifies memory reserved for IHV use and the input data for the DRM command.


### -field Status

The result of the hardware DRM command.


## -remarks



A pointer to this structure is passed in the <i>pData</i> parameter of <a href="https://msdn.microsoft.com/76160B03-6F7F-4618-859B-0A7E73540CA4">ID3D11VideoContext::NegotiateCryptoSessionKeyExchange</a> method when the <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> is creating using the <b>D3D11_KEY_EXCHANGE_HW_PROTECTION</b> key exchange type.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

