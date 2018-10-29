---
UID: NS:d3d11.D3D11_VIDEO_CONTENT_PROTECTION_CAPS
title: D3D11_VIDEO_CONTENT_PROTECTION_CAPS
author: windows-sdk-content
description: Describes the content-protection capabilities of a graphics driver.
old-location: mf\d3d11_video_content_protection_caps.htm
tech.root: medfound
ms.assetid: 15691779-DC30-4C0C-86D0-497F2BD60614
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: D3D11_VIDEO_CONTENT_PROTECTION_CAPS, D3D11_VIDEO_CONTENT_PROTECTION_CAPS structure [Media Foundation], d3d11/D3D11_VIDEO_CONTENT_PROTECTION_CAPS, mf.d3d11_video_content_protection_caps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - D3D11_VIDEO_CONTENT_PROTECTION_CAPS
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_CONTENT_PROTECTION_CAPS
req.redist: 
---

# D3D11_VIDEO_CONTENT_PROTECTION_CAPS structure


## -description


Describes the content-protection capabilities of a graphics driver.


## -struct-fields




### -field Caps

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/en-us/library/Hh447629(v=VS.85).aspx">D3D11_CONTENT_PROTECTION_CAPS</a> enumeration.


### -field KeyExchangeTypeCount

The number of cryptographic key-exchange types that are supported by the driver. To get the list of key-exchange types, call the <a href="https://msdn.microsoft.com/en-us/library/Hh447782(v=VS.85).aspx">ID3D11VideoDevice::CheckCryptoKeyExchange</a> method.


### -field BlockAlignmentSize

The encyrption block size, in bytes. The size of data to be encrypted must be a multiple of this value. 


### -field ProtectedMemorySize

The total amount of memory, in bytes, that can be used to hold protected surfaces.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447680(v=VS.85).aspx">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh447792(v=VS.85).aspx">ID3D11VideoDevice::GetContentProtectionCaps</a>
 

 

