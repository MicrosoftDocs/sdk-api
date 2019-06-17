---
UID: NE:mfapi._MFWaveFormatExConvertFlags
title: MFWaveFormatExConvertFlags (mfapi.h)
author: windows-sdk-content
description: Contains flags that specify how to convert an audio media type.
old-location: mf\mfwaveformatexconvertflags.htm
tech.root: medfound
ms.assetid: cd4a54f3-58e5-4e39-8615-e5037972c9c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFWaveFormatExConvertFlag_ForceExtensible, MFWaveFormatExConvertFlag_Normal, MFWaveFormatExConvertFlags, MFWaveFormatExConvertFlags enumeration [Media Foundation], cd4a54f3-58e5-4e39-8615-e5037972c9c4, mf.mfwaveformatexconvertflags, mfapi/MFWaveFormatExConvertFlag_ForceExtensible, mfapi/MFWaveFormatExConvertFlag_Normal, mfapi/MFWaveFormatExConvertFlags
ms.topic: enum
f1_keywords: ["mfapi/MFWaveFormatExConvertFlags"]
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfapi.h
api_name:
 - MFWaveFormatExConvertFlags
product: Windows
targetos: Windows
req.typenames: MFWaveFormatExConvertFlags
req.redist: 
ms.custom: 19H1
---

# MFWaveFormatExConvertFlags enumeration


## -description



Contains flags that specify how to convert an audio media type.




## -enum-fields




### -field MFWaveFormatExConvertFlag_Normal

Convert the media type to a <b>WAVEFORMATEX</b> structure if possible, or a <b>WAVEFORMATEXTENSIBLE</b> structure otherwise.


### -field MFWaveFormatExConvertFlag_ForceExtensible

Convert the media type to a <b>WAVEFORMATEXTENSIBLE</b> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype">MFCreateWaveFormatExFromMFMediaType</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

