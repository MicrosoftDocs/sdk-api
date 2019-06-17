---
UID: NS:mfobjects.__MIDL___MIDL_itf_mfobjects_0000_0008_0003
title: MFT_REGISTER_TYPE_INFO (mfobjects.h)
author: windows-sdk-content
description: Contains media type information for registering a Media Foundation transform (MFT).
old-location: mf\mft_register_type_info.htm
tech.root: medfound
ms.assetid: 1d26b9ee-545a-4e47-9a68-b9e567f0dec4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1d26b9ee-545a-4e47-9a68-b9e567f0dec4, MFT_REGISTER_TYPE_INFO, MFT_REGISTER_TYPE_INFO structure [Media Foundation], _MFT_REGISTER_TYPE_INFO, mf.mft_register_type_info, mfobjects/MFT_REGISTER_TYPE_INFO
ms.topic: struct
f1_keywords: ["mfobjects/MFT_REGISTER_TYPE_INFO"]
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfobjects.h
api_name:
 - MFT_REGISTER_TYPE_INFO
product: Windows
targetos: Windows
req.typenames: MFT_REGISTER_TYPE_INFO
req.redist: 
ms.custom: 19H1
---

# MFT_REGISTER_TYPE_INFO structure


## -description


Contains media type information for registering a Media Foundation transform (MFT).
        


## -struct-fields




### -field guidMajorType

The major media type. For a list of possible values, see <a href="https://docs.microsoft.com/windows/desktop/medfound/media-type-guids">Major Media Types</a>.
          


### -field guidSubtype

The media subtype. For a list of possible values, see the following topics:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/audio-subtype-guids">Audio Subtype GUIDs</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/medfound/video-subtype-guids">Video Subtype GUIDs</a>
</li>
</ul>

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenum">MFTEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo">MFTGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

