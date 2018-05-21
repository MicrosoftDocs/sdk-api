---
UID: NS:d3d11.D3D11_VIDEO_CONTENT_PROTECTION_CAPS
title: D3D11_VIDEO_CONTENT_PROTECTION_CAPS
author: windows-driver-content
description: Describes the content-protection capabilities of a graphics driver.
old-location: mf\d3d11_video_content_protection_caps.htm
old-project: medfound
ms.assetid: 15691779-DC30-4C0C-86D0-497F2BD60614
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: D3D11_VIDEO_CONTENT_PROTECTION_CAPS, D3D11_VIDEO_CONTENT_PROTECTION_CAPS structure [Media Foundation], d3d11/D3D11_VIDEO_CONTENT_PROTECTION_CAPS, mf.d3d11_video_content_protection_caps
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: D3D11_VIDEO_CONTENT_PROTECTION_CAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_VIDEO_CONTENT_PROTECTION_CAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_CONTENT_PROTECTION_CAPS structure


## -description


Describes the content-protection capabilities of a graphics driver.


## -struct-fields




### -field Caps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/19697660-DDB8-4A4C-888F-018BC5CCFC94">D3D11_CONTENT_PROTECTION_CAPS</a> enumeration.


### -field KeyExchangeTypeCount

The number of cryptographic key-exchange types that are supported by the driver. To get the list of key-exchange types, call the <a href="https://msdn.microsoft.com/AE2DA6F9-6153-43AF-8E61-26FB9DD5A1D1">ID3D11VideoDevice::CheckCryptoKeyExchange</a> method.


### -field BlockAlignmentSize

The encyrption block size, in bytes. The size of data to be encrypted must be a multiple of this value. 


### -field ProtectedMemorySize

The total amount of memory, in bytes, that can be used to hold protected surfaces.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/3BF2D2B9-6A12-4E71-9F52-829BABA32EF6">ID3D11VideoDevice::GetContentProtectionCaps</a>
 

 

