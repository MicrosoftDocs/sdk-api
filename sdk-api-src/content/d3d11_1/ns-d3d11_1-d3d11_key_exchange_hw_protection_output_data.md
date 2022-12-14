---
UID: NS:d3d11_1.D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
title: D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA (d3d11_1.h)
description: Represents key exchange output data for hardware content protection.
helpviewer_keywords: ["D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA","D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA structure [Media Foundation]","d3d11_1/D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA","mf.d3d11_key_exchange_hw_protection_output_data"]
old-location: mf\d3d11_key_exchange_hw_protection_output_data.htm
tech.root: mf
ms.assetid: D8F987CA-0BD2-42D1-AE95-8D2D118655B1
ms.date: 12/05/2018
ms.keywords: D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA, D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA structure [Media Foundation], d3d11_1/D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA, mf.d3d11_key_exchange_hw_protection_output_data
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
targetos: Windows
req.typenames: D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
 - d3d11_1/D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA
---

# D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA structure


## -description

Represents key exchange output data for hardware content protection.

## -struct-fields

### -field PrivateDataSize

The size of the private data reserved for IHV usage. This size is determined from the <i>pPrivateOutputSize</i> parameter returned by the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getcryptosessionprivatedatasize">ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize</a> function.

### -field MaxHWProtectionDataSize

The maximum size of data that the driver can return in the output buffer. The last byte that it can write to is <b>pbOutput</b>[<b>PrivateDataSize</b> + <b>MaxHWProtectionDataSize</b> – 1].

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

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>