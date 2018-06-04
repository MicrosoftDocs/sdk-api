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

# ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize


## -description


Retrieves optional sizes for private driver data. 


## -parameters




### -param pCryptoType [in]

Type: <b>const GUID*</b>

Indicates the crypto type for which the private input and output size is queried.


### -param pDecoderProfile [in, optional]

Type: <b>const GUID*</b>

Indicates the decoder profile for which the private input and output size is queried.


### -param pKeyExchangeType [in]

Type: <b>const GUID*</b>

Indicates the key exchange type for which the private input and output size is queried.


### -param pPrivateInputSize [out]

Type: <b>UINT*</b>

Returns the size of private data that the driver needs for input commands.


### -param pPrivateOutputSize [out]

Type: <b>UINT*</b>

Returns the size of private data that the driver needs for output commands.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.




## -remarks



When <i>pKeyExchangeType</i> is <b>D3D11_KEY_EXCHANGE_HW_PROTECTION</b>, the following behavior is expected in the <a href="https://msdn.microsoft.com/76160B03-6F7F-4618-859B-0A7E73540CA4">ID3D11VideoContext::NegotiateCryptoSessionKeyExchange</a> method:

<ul>
<li>The <i>DataSize</i> parameter is set to the size of the <a href="https://msdn.microsoft.com/1DAAE15F-80E4-4645-8326-0ECB1809F8CF">D3D11_KEY_EXCHANGE_HW_PROTECTION_DATA</a> structure.</li>
<li><i>pData</i> points to a <a href="https://msdn.microsoft.com/1DAAE15F-80E4-4645-8326-0ECB1809F8CF">D3D11_KEY_EXCHANGE_HW_PROTECTION_DATA</a> structure. <ul>
<li>The <b>pInputData</b> of this structure points to a <a href="https://msdn.microsoft.com/B3F587BC-0DA8-496B-A3F5-ADFD16ABABB9">D3D11_KEY_EXCHANGE_HW_PROTECTION_INPUT_DATA</a> structure where:<ul>
<li><b>pbInput</b>[0] – <b>pbInput</b>[N-1] contains memory reserved for use by the driver. The number of bytes (N) reserved for the driver is determined by the <b>pPrivateInputSize</b> value returned by the <b>ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize</b> function.</li>
<li><b>pbInput</b>[N] contains the first byte of the DRM command packet.</li>
</ul>
</li>
<li>The <b>pOutputData</b> of this structure points to a <a href="https://msdn.microsoft.com/D8F987CA-0BD2-42D1-AE95-8D2D118655B1">D3D11_KEY_EXCHANGE_HW_PROTECTION_OUTPUT_DATA</a> structure where:<ul>
<li><b>pbOutput</b>[0] – <b>pbOutput</b>[N-1] contains memory reserved for use by the driver. The number of bytes (N) reserved for the driver is determined by the <b>pPrivateOutputSize</b> value returned by the <b>ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize</b> function.</li>
<li><b>pbOutput</b>[N] contains the first byte of the DRM command packet.</li>
</ul>
</li>
</ul>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/10E68945-6103-491D-8846-3B7C880FEAFD">ID3D11VideoDevice1</a>
 

 

