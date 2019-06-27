---
UID: NE:codecapi.eAVEncVideoOutputFrameRateConversion
title: eAVEncVideoOutputFrameRateConversion (codecapi.h)
author: windows-sdk-content
description: Specifies whether the encoder converts the frame rate, if the output frame rate does not match the input frame rate. This enumeration is used with the AVEncVideoOutputFrameRateConversion property.
old-location: dshow\eavencvideooutputframerateconversion.htm
tech.root: DirectShow
ms.assetid: 0303f49c-9651-4781-8a6b-2af0a1b8f1ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoOutputFrameRateConversion, codecapi/eAVEncVideoOutputFrameRateConversion_Alias, codecapi/eAVEncVideoOutputFrameRateConversion_Disable, codecapi/eAVEncVideoOutputFrameRateConversion_Enable, dshow.eavencvideooutputframerateconversion, eAVEncVideoOutputFrameRateConversion, eAVEncVideoOutputFrameRateConversion enumeration [DirectShow], eAVEncVideoOutputFrameRateConversionEnumeration, eAVEncVideoOutputFrameRateConversion_Alias, eAVEncVideoOutputFrameRateConversion_Disable, eAVEncVideoOutputFrameRateConversion_Enable
ms.topic: enum
f1_keywords: 
 - "codecapi/eAVEncVideoOutputFrameRateConversion"
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - codecapi.h
api_name:
 - eAVEncVideoOutputFrameRateConversion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncVideoOutputFrameRateConversion enumeration


## -description



Specifies whether the encoder converts the frame rate, if the output frame rate does not match the input frame rate. This enumeration is used with the <b>AVEncVideoOutputFrameRateConversion</b> property.




## -enum-fields




### -field eAVEncVideoOutputFrameRateConversion_Disable

Disable frame rate conversion.


### -field eAVEncVideoOutputFrameRateConversion_Enable

Enable frame rate conversion.


### -field eAVEncVideoOutputFrameRateConversion_Alias

Change the time stamps on the samples, but do not interpolate the time stamps.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

