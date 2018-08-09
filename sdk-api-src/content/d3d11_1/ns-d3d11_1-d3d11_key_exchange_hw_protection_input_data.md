---
UID: NS:d3d11_1.D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA
title: D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA
author: windows-sdk-content
description: Represents key exchange input data for hardware content protection.
old-location: mf\d3d11_key_exchange_hw_protection_input_data.htm
old-project: medfound
ms.assetid: B3F587BC-0DA8-496B-A3F5-ADFD16ABABB9
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA, D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA structure [Media Foundation], d3d11_1/D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA, mf.d3d11_key_exchange_hw_protection_input_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA structure


## -description


Represents key exchange input data for hardware content protection.


## -struct-fields




### -field PrivateDataSize

The size of the private data reserved for IHV usage. This size is determined from the <i>pPrivateInputSize</i> parameter returned by the <a href="https://msdn.microsoft.com/3F973DA0-F722-4EC2-A578-F01B6999F16B">ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize</a> function.


### -field HWProtectionDataSize

The size of the DRM command data.


### -field pbInput

If <b>PrivateDataSize</b> is greater than 0,  pbInput[0] – <b>pbInput</b>[<b>PrivateDataSize</b> - 1] is reserved for IHV use.

<b>pbInput</b>[<b>PrivateDataSize</b>] – <b>pbInput</b>[<b>HWProtectionDataSize</b> + <b>PrivateDataSize</b> - 1] contains the input data for the DRM command. The format and size of the DRM command is defined by the DRM specification.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

