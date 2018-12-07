---
UID: NE:mfapi._MFWaveFormatExConvertFlags
title: "_MFWaveFormatExConvertFlags"
author: windows-sdk-content
description: Contains flags that specify how to convert an audio media type.
old-location: mf\mfwaveformatexconvertflags.htm
tech.root: medfound
ms.assetid: cd4a54f3-58e5-4e39-8615-e5037972c9c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFWaveFormatExConvertFlag_ForceExtensible, MFWaveFormatExConvertFlag_Normal, MFWaveFormatExConvertFlags, MFWaveFormatExConvertFlags enumeration [Media Foundation], _MFWaveFormatExConvertFlags, cd4a54f3-58e5-4e39-8615-e5037972c9c4, mf.mfwaveformatexconvertflags, mfapi/MFWaveFormatExConvertFlag_ForceExtensible, mfapi/MFWaveFormatExConvertFlag_Normal, mfapi/MFWaveFormatExConvertFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
---

# _MFWaveFormatExConvertFlags enumeration


## -description



Contains flags that specify how to convert an audio media type.




## -enum-fields




### -field MFWaveFormatExConvertFlag_Normal

Convert the media type to a <b>WAVEFORMATEX</b> structure if possible, or a <b>WAVEFORMATEXTENSIBLE</b> structure otherwise.


### -field MFWaveFormatExConvertFlag_ForceExtensible

Convert the media type to a <b>WAVEFORMATEXTENSIBLE</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/b124bac2-90de-4358-a079-f509a89c3776">MFCreateWaveFormatExFromMFMediaType</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

