---
UID: NE:mfapi._MFWaveFormatExConvertFlags
title: MFWaveFormatExConvertFlags (mfapi.h)
description: Contains flags that specify how to convert an audio media type.
helpviewer_keywords: ["MFWaveFormatExConvertFlag_ForceExtensible","MFWaveFormatExConvertFlag_Normal","MFWaveFormatExConvertFlags","MFWaveFormatExConvertFlags enumeration [Media Foundation]","cd4a54f3-58e5-4e39-8615-e5037972c9c4","mf.mfwaveformatexconvertflags","mfapi/MFWaveFormatExConvertFlag_ForceExtensible","mfapi/MFWaveFormatExConvertFlag_Normal","mfapi/MFWaveFormatExConvertFlags"]
old-location: mf\mfwaveformatexconvertflags.htm
tech.root: mf
ms.assetid: cd4a54f3-58e5-4e39-8615-e5037972c9c4
ms.date: 12/05/2018
ms.keywords: MFWaveFormatExConvertFlag_ForceExtensible, MFWaveFormatExConvertFlag_Normal, MFWaveFormatExConvertFlags, MFWaveFormatExConvertFlags enumeration [Media Foundation], cd4a54f3-58e5-4e39-8615-e5037972c9c4, mf.mfwaveformatexconvertflags, mfapi/MFWaveFormatExConvertFlag_ForceExtensible, mfapi/MFWaveFormatExConvertFlag_Normal, mfapi/MFWaveFormatExConvertFlags
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
targetos: Windows
req.typenames: MFWaveFormatExConvertFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFWaveFormatExConvertFlags
 - mfapi/_MFWaveFormatExConvertFlags
 - MFWaveFormatExConvertFlags
 - mfapi/MFWaveFormatExConvertFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFWaveFormatExConvertFlags
---

# MFWaveFormatExConvertFlags enumeration


## -description

Contains flags that specify how to convert an audio media type.

## -enum-fields

### -field MFWaveFormatExConvertFlag_Normal:0

Convert the media type to a <b>WAVEFORMATEX</b> structure if possible, or a <b>WAVEFORMATEXTENSIBLE</b> structure otherwise.

### -field MFWaveFormatExConvertFlag_ForceExtensible:1

Convert the media type to a <b>WAVEFORMATEXTENSIBLE</b> structure.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype">MFCreateWaveFormatExFromMFMediaType</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
