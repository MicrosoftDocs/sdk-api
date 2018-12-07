---
UID: NS:d3d11_1.D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
title: D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
author: windows-sdk-content
description: Represents key exchange output data for hardware content protection.
old-location: mf\d3d11_key_exchange_hw_protection_output_data.htm
tech.root: medfound
ms.assetid: D8F987CA-0BD2-42D1-AE95-8D2D118655B1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA, D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA structure [Media Foundation], d3d11_1/D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA, mf.d3d11_key_exchange_hw_protection_output_data
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
product: Windows
targetos: Windows
req.typenames: D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
req.redist: 
---

# D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA structure


## -description


Represents key exchange output data for hardware content protection.


## -struct-fields




### -field PrivateDataSize

The size of the private data reserved for IHV usage. This size is determined from the <i>pPrivateOutputSize</i> parameter returned by the <a href="https://msdn.microsoft.com/en-us/library/Dn894143(v=VS.85).aspx">ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize</a> function.


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




<a href="https://msdn.microsoft.com/en-us/library/Hh447680(v=VS.85).aspx">Direct3D 11 Video Structures</a>
 

 

