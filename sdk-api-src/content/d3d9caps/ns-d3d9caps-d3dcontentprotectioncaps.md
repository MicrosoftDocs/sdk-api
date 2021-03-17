---
UID: NS:d3d9caps._D3DCONTENTPROTECTIONCAPS
title: D3DCONTENTPROTECTIONCAPS (d3d9caps.h)
description: Describes the content protection capabilities of a display driver.
helpviewer_keywords: ["D3DCONTENTPROTECTIONCAPS","D3DCONTENTPROTECTIONCAPS structure [Media Foundation]","D3DCPCAPS_CONTENTKEY","D3DCPCAPS_ENCRYPTEDREADBACK","D3DCPCAPS_ENCRYPTEDREADBACKKEY","D3DCPCAPS_FRESHENSESSIONKEY","D3DCPCAPS_HARDWARE","D3DCPCAPS_PARTIALDECRYPTION","D3DCPCAPS_PROTECTIONALWAYSON","D3DCPCAPS_SEQUENTIAL_CTR_IV","D3DCPCAPS_SOFTWARE","D3DKEYEXCHANGE_DXVA","D3DKEYEXCHANGE_RSAES_OAEP","d3d9caps/D3DCONTENTPROTECTIONCAPS","mf.d3dcontentprotectioncaps"]
old-location: mf\d3dcontentprotectioncaps.htm
tech.root: mf
ms.assetid: 73ef2e12-d376-4bc2-a940-d421acfdd43e
ms.date: 12/05/2018
ms.keywords: D3DCONTENTPROTECTIONCAPS, D3DCONTENTPROTECTIONCAPS structure [Media Foundation], D3DCPCAPS_CONTENTKEY, D3DCPCAPS_ENCRYPTEDREADBACK, D3DCPCAPS_ENCRYPTEDREADBACKKEY, D3DCPCAPS_FRESHENSESSIONKEY, D3DCPCAPS_HARDWARE, D3DCPCAPS_PARTIALDECRYPTION, D3DCPCAPS_PROTECTIONALWAYSON, D3DCPCAPS_SEQUENTIAL_CTR_IV, D3DCPCAPS_SOFTWARE, D3DKEYEXCHANGE_DXVA, D3DKEYEXCHANGE_RSAES_OAEP, d3d9caps/D3DCONTENTPROTECTIONCAPS, mf.d3dcontentprotectioncaps
req.header: d3d9caps.h
req.include-header: D3d9.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: D3DCONTENTPROTECTIONCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3DCONTENTPROTECTIONCAPS
 - d3d9caps/_D3DCONTENTPROTECTIONCAPS
 - D3DCONTENTPROTECTIONCAPS
 - d3d9caps/D3DCONTENTPROTECTIONCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d9caps.h
api_name:
 - D3DCONTENTPROTECTIONCAPS
---

# D3DCONTENTPROTECTIONCAPS structure


## -description

Describes the content protection capabilities of a display driver. To get the capabilities, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a>.

## -struct-fields

### -field Caps

Bitwise <b>OR</b> of zero or more flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_SOFTWARE"></a><a id="d3dcpcaps_software"></a><dl>
<dt><b>D3DCPCAPS_SOFTWARE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The encryption is implemented in software by the driver. 

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_HARDWARE"></a><a id="d3dcpcaps_hardware"></a><dl>
<dt><b>D3DCPCAPS_HARDWARE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The encryption is implemented in hardware by the GPU.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_PROTECTIONALWAYSON"></a><a id="d3dcpcaps_protectionalwayson"></a><dl>
<dt><b>D3DCPCAPS_PROTECTIONALWAYSON</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Content protection is always applied to a protected Direct3D surface, regardless of whether the application explicitly enables content protection.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_PARTIALDECRYPTION"></a><a id="d3dcpcaps_partialdecryption"></a><dl>
<dt><b>D3DCPCAPS_PARTIALDECRYPTION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The driver can use partially encrypted buffers. If this capability is not present, the entire buffer must be either encrypted or clear.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_CONTENTKEY"></a><a id="d3dcpcaps_contentkey"></a><dl>
<dt><b>D3DCPCAPS_CONTENTKEY</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The driver can encrypt data using a separate content key that is encrypted using the session key. For more information, see <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-decryptionblt">IDirect3DCryptoSession9::DecryptionBlt</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_FRESHENSESSIONKEY"></a><a id="d3dcpcaps_freshensessionkey"></a><dl>
<dt><b>D3DCPCAPS_FRESHENSESSIONKEY</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The driver can refresh the session key without renegotiating the key. To refresh the session key, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-startsessionkeyrefresh">IDirect3DCryptoSession9::StartSessionKeyRefresh</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_ENCRYPTEDREADBACK"></a><a id="d3dcpcaps_encryptedreadback"></a><dl>
<dt><b>D3DCPCAPS_ENCRYPTEDREADBACK</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The driver can read back encrypted data from a protected surface, using the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-encryptionblt">IDirect3DCryptoSession9::EncryptionBlt</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_ENCRYPTEDREADBACKKEY"></a><a id="d3dcpcaps_encryptedreadbackkey"></a><dl>
<dt><b>D3DCPCAPS_ENCRYPTEDREADBACKKEY</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The driver requires a separate key to read encrypted data from a protected surface. To get this second key, call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getencryptionbltkey">IDirect3DCryptoSession9::GetEncryptionBltKey</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="D3DCPCAPS_SEQUENTIAL_CTR_IV"></a><a id="d3dcpcaps_sequential_ctr_iv"></a><dl>
<dt><b>D3DCPCAPS_SEQUENTIAL_CTR_IV</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
If the encryption type is <b>D3DCRYPTOTYPE_AES128_CTR</b>, the application must use a sequential count in the <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv">DXVA2_AES_CTR_IV</a>  structure. For more information, see the remarks for <b>DXVA2_AES_CTR_IV</b>.

</td>
</tr>
</table>

### -field KeyExchangeType

Specifies the type of key exchange required to negotiate the session key. The following GUIDs are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3DKEYEXCHANGE_RSAES_OAEP"></a><a id="d3dkeyexchange_rsaes_oaep"></a><dl>
<dt><b>D3DKEYEXCHANGE_RSAES_OAEP</b></dt>
</dl>
</td>
<td width="60%">
The decoder encrypts the session key using RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP).

</td>
</tr>
<tr>
<td width="40%"><a id="D3DKEYEXCHANGE_DXVA"></a><a id="d3dkeyexchange_dxva"></a><dl>
<dt><b>D3DKEYEXCHANGE_DXVA</b></dt>
</dl>
</td>
<td width="60%">
Use the key exchange mechanism defined for DirectX Video Acceleration 2 (DXVA-2). 

</td>
</tr>
</table>

### -field BufferAlignmentStart

The memory alignment required for buffers used by the GPU cryptographic engine. If the application uses a system memory buffer to pass encrypted content to the GPU, or to read back encrypted content from the GPU, the buffer's starting address must be a multiple of this value.

### -field BlockAlignmentSize

The block alignment required by the GPU cryptographic engine. The size of data to be encrypted must be a multiple of this value.

### -field ProtectedMemorySize

The total amount of memory that can be used to hold protected surfaces.

## -see-also

<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps">IDirect3DDevice9Video::GetContentProtectionCaps</a>