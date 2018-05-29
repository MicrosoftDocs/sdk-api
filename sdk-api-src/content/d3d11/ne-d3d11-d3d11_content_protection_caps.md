---
UID: NE:d3d11.D3D11_CONTENT_PROTECTION_CAPS
title: D3D11_CONTENT_PROTECTION_CAPS
author: windows-sdk-content
description: Contains flags that describe content-protection capabilities.
old-location: mf\d3d11_content_protection_caps.htm
old-project: medfound
ms.assetid: 19697660-DDB8-4A4C-888F-018BC5CCFC94
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: D3D11_CONTENT_PROTECTION_CAPS, D3D11_CONTENT_PROTECTION_CAPS enumeration [Media Foundation], D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY, D3D11_CONTENT_PROTECTION_CAPS_DECRYPTION_BLT, D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK, D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK_KEY, D3D11_CONTENT_PROTECTION_CAPS_ENCRYPT_SLICEDATA_ONLY, D3D11_CONTENT_PROTECTION_CAPS_FRESHEN_SESSION_KEY, D3D11_CONTENT_PROTECTION_CAPS_HARDWARE, D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_DRM_COMMUNICATION, D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_PROTECTED_MEMORY_PAGEABLE, D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_PROTECT_UNCOMPRESSED, D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_TEARDOWN, D3D11_CONTENT_PROTECTION_CAPS_PARTIAL_DECRYPTION, D3D11_CONTENT_PROTECTION_CAPS_PROTECTION_ALWAYS_ON, D3D11_CONTENT_PROTECTION_CAPS_SEQUENTIAL_CTR_IV, D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE, d3d11/ D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_PROTECT_UNCOMPRESSED, d3d11/D3D11_CONTENT_PROTECTION_CAPS, d3d11/D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY, d3d11/D3D11_CONTENT_PROTECTION_CAPS_DECRYPTION_BLT, d3d11/D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK, d3d11/D3D11_CONTENT_PROTECTION_CAPS_ENCRYPTED_READ_BACK_KEY, d3d11/D3D11_CONTENT_PROTECTION_CAPS_ENCRYPT_SLICEDATA_ONLY, d3d11/D3D11_CONTENT_PROTECTION_CAPS_FRESHEN_SESSION_KEY, d3d11/D3D11_CONTENT_PROTECTION_CAPS_HARDWARE, d3d11/D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_DRM_COMMUNICATION, d3d11/D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_PROTECTED_MEMORY_PAGEABLE, d3d11/D3D11_CONTENT_PROTECTION_CAPS_HARDWARE_TEARDOWN, d3d11/D3D11_CONTENT_PROTECTION_CAPS_PARTIAL_DECRYPTION, d3d11/D3D11_CONTENT_PROTECTION_CAPS_PROTECTION_ALWAYS_ON, d3d11/D3D11_CONTENT_PROTECTION_CAPS_SEQUENTIAL_CTR_IV, d3d11/D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE, mf.d3d11_content_protection_caps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_CONTENT_PROTECTION_CAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_CONTENT_PROTECTION_CAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

