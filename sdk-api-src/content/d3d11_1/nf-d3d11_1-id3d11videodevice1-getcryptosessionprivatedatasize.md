---
UID: NF:d3d11_1.ID3D11VideoDevice1.GetCryptoSessionPrivateDataSize
title: ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize
author: windows-driver-content
description: Retrieves optional sizes for private driver data.
old-location: mf\id3d11videodevice1_getcryptosessionprivatedatasize.htm
old-project: medfound
ms.assetid: 3F973DA0-F722-4EC2-A578-F01B6999F16B
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetCryptoSessionPrivateDataSize, GetCryptoSessionPrivateDataSize method [Media Foundation], GetCryptoSessionPrivateDataSize method [Media Foundation],ID3D11VideoDevice1 interface, ID3D11VideoDevice1 interface [Media Foundation],GetCryptoSessionPrivateDataSize method, ID3D11VideoDevice1.GetCryptoSessionPrivateDataSize, ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize, d3d11_1/ID3D11VideoDevice1::GetCryptoSessionPrivateDataSize, mf.id3d11videodevice1_getcryptosessionprivatedatasize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11_1.h
api_name:
-	ID3D11VideoDevice1.GetCryptoSessionPrivateDataSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

