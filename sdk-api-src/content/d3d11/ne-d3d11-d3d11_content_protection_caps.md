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

# D3D11_CONTENT_PROTECTION_CAPS enumeration


## -description


Contains flags that describe content-protection capabilities.


## -enum-fields




### -field D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE

The content protection is implemented in software by the driver.


### -field D3D11_CONTENT_PROTECTION_CAPS_HARDWARE

The content protection is implemented in hardware by the GPU.



### -field D3D11_CONTENT_PROTECTION_CAPS_PROTECTION_ALWAYS_ON

Content protection is always applied to a protected surface, regardless of whether the application explicitly enables protection.


### -field D3D11_CONTENT_PROTECTION_CAPS_PARTIAL_DECRYPTION

The driver can use partially encrypted buffers. If this capability is not present, the entire buffer must be either encrypted or clear.


### -field D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY

The driver can encrypt data using a separate content key that is encrypted using the session key.


### -field D3D11_CONTENT_PROTECTION_CAPS_FRESHEN_SESSION_KEY

The driver can refresh the session key without renegotiating the key.


### -field D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK

The driver can read back encrypted data from a protected surface. For more information, see <a href="https://msdn.microsoft.com/2BBD0BC2-53D9-435E-835C-20A992118329">ID3D11VideoContext::EncryptionBlt</a>.


### -field D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK_KEY

The driver requires a separate key to read encrypted data from a protected surface.


### -field D3D11_CONTENT_PROTECTION_CAPS_SEQUENTIAL_CTR_IV

If the encryption type is <b>D3DCRYPTOTYPE_AES128_CTR</b>, the application must use a sequential count in the <a href="https://msdn.microsoft.com/2D1B24CA-6386-4406-9195-40913744C9CF">D3D11_AES_CTR_IV</a>  structure.


### -field D3D11_CONTENT_PROTECTION_CAPS_ENCRYPT_SLICEDATA_ONLY

The driver supports encrypted slice data, but does not support any other encrypted data in the compressed buffer.  The caller should not encrypt any data within the buffer other than the slice data.

<div class="alert"><b>Note</b>  The driver should only report this flag for the specific profiles that have this limitation.</div>
<div> </div>

### -field D3D11_CONTENT_PROTECTION_CAPS_DECRYPTION_BLT

The driver can copy encrypted data from one resource to another, decrypting the data as part of the process.


### -field D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_PROTECT_UNCOMPRESSED

The hardware supports the protection of specific resources. This means that:

<ul>
<li>The contents of a protected allocation can never be read by the CPU.</li>
<li>The hardware can ensure a protected resource cannot be copied to an unprotected resource.</li>
</ul>
<b>Note</b>  This enumeration value is supported starting with Windows 10.


### -field D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_PROTECTED_MEMORY_PAGEABLE

Physical pages of a protected resource can be evicted and potentially paged to disk in low memory conditions without losing the contents of the resource when paged back in. 

<b>Note</b>  This enumeration value is supported starting with Windows 10.


### -field D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_TEARDOWN

The hardware supports an automatic teardown mechanism that could trigger hardware keys or protected content to become lost in some conditions.  The application can register to be notified when these events occur.

<b>Note</b>  This enumeration value is supported starting with Windows 10.


### -field D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_DRM_COMMUNICATION

The secure environment is tightly coupled with the GPU and an <a href="https://msdn.microsoft.com/E17F39CB-61E3-44EF-805D-AD386743744E">ID3D11CryptoSession</a> should be used for communication between the user mode DRM component and the secure execution environment.

<b>Note</b>  This enumeration value is supported starting with Windows 10.


### -field D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_DRM_COMMUNICATION_MULTI_THREADED




## -see-also




<a href="https://msdn.microsoft.com/15691779-DC30-4C0C-86D0-497F2BD60614">D3D11_VIDEO_CONTENT_PROTECTION_CAPS</a>



<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>
 

 

