---
UID: NS:d3d11.D3D11_VIDEO_CONTENT_PROTECTION_CAPS
title: D3D11_VIDEO_CONTENT_PROTECTION_CAPS (d3d11.h)
description: Describes the content-protection capabilities of a graphics driver.
helpviewer_keywords: ["D3D11_VIDEO_CONTENT_PROTECTION_CAPS","D3D11_VIDEO_CONTENT_PROTECTION_CAPS structure [Media Foundation]","d3d11/D3D11_VIDEO_CONTENT_PROTECTION_CAPS","mf.d3d11_video_content_protection_caps"]
old-location: mf\d3d11_video_content_protection_caps.htm
tech.root: mf
ms.assetid: 15691779-DC30-4C0C-86D0-497F2BD60614
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_CONTENT_PROTECTION_CAPS, D3D11_VIDEO_CONTENT_PROTECTION_CAPS structure [Media Foundation], d3d11/D3D11_VIDEO_CONTENT_PROTECTION_CAPS, mf.d3d11_video_content_protection_caps
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
targetos: Windows
req.typenames: D3D11_VIDEO_CONTENT_PROTECTION_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_CONTENT_PROTECTION_CAPS
 - d3d11/D3D11_VIDEO_CONTENT_PROTECTION_CAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_CONTENT_PROTECTION_CAPS
---

# D3D11_VIDEO_CONTENT_PROTECTION_CAPS structure


## -description

Describes the content-protection capabilities of a graphics driver.

## -struct-fields

### -field Caps

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_content_protection_caps">D3D11_CONTENT_PROTECTION_CAPS</a> enumeration.

### -field KeyExchangeTypeCount

The number of cryptographic key-exchange types that are supported by the driver. To get the list of key-exchange types, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange">ID3D11VideoDevice::CheckCryptoKeyExchange</a> method.

### -field BlockAlignmentSize

The encryption block size, in bytes. The size of data to be encrypted must be a multiple of this value.

### -field ProtectedMemorySize

The total amount of memory, in bytes, that can be used to hold protected surfaces.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps">ID3D11VideoDevice::GetContentProtectionCaps</a>