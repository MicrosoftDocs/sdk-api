---
UID: NE:dxvahd._DXVAHD_FEATURE_CAPS
title: "_DXVAHD_FEATURE_CAPS"
author: windows-sdk-content
description: Defines features that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device can support.
old-location: mf\dxvahd_feature_caps.htm
old-project: medfound
ms.assetid: 6014780b-3b8a-48d6-ae30-b48127a2c274
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DXVAHD_FEATURE_CAPS, DXVAHD_FEATURE_CAPS enumeration [Media Foundation], DXVAHD_FEATURE_CAPS_ALPHA_FILL, DXVAHD_FEATURE_CAPS_ALPHA_PALETTE, DXVAHD_FEATURE_CAPS_CONSTRICTION, DXVAHD_FEATURE_CAPS_LUMA_KEY, _DXVAHD_FEATURE_CAPS, dxvahd/DXVAHD_FEATURE_CAPS, dxvahd/DXVAHD_FEATURE_CAPS_ALPHA_FILL, dxvahd/DXVAHD_FEATURE_CAPS_ALPHA_PALETTE, dxvahd/DXVAHD_FEATURE_CAPS_CONSTRICTION, dxvahd/DXVAHD_FEATURE_CAPS_LUMA_KEY, mf.dxvahd_feature_caps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxvahd.h
req.include-header: 
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
tech.root: 
req.typenames: DXVAHD_FEATURE_CAPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_FEATURE_CAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_FEATURE_CAPS enumeration


## -description


Defines features that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device can support.


## -enum-fields




### -field DXVAHD_FEATURE_CAPS_ALPHA_FILL

The device can set the alpha values on the video output. See <a href="https://msdn.microsoft.com/dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>.


### -field DXVAHD_FEATURE_CAPS_CONSTRICTION

The device can downsample the video output. See <a href="https://msdn.microsoft.com/962a99bd-060d-4101-b65a-d0406e136bf7">DXVAHD_BLT_STATE_CONSTRICTION_DATA</a>.


### -field DXVAHD_FEATURE_CAPS_LUMA_KEY

The device can perform luma keying. See <a href="https://msdn.microsoft.com/d94b04d9-9d94-4392-a0bf-a33210aeef1f">DXVAHD_STREAM_STATE_LUMA_KEY_DATA</a>.


### -field DXVAHD_FEATURE_CAPS_ALPHA_PALETTE

The device can apply alpha values from color palette entries. See <a href="https://msdn.microsoft.com/51135d6e-4f97-44d9-b1d5-f7d2095ee6f1">DXVAHD_STREAM_STATE_ALPHA_DATA</a>.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

