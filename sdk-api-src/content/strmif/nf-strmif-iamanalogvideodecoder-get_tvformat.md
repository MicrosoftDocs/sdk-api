---
UID: NF:strmif.IAMAnalogVideoDecoder.get_TVFormat
title: IAMAnalogVideoDecoder::get_TVFormat (strmif.h)
author: windows-sdk-content
description: The get_TVFormat method retrieves the current analog video format.
old-location: dshow\iamanalogvideodecoder_get_tvformat.htm
tech.root: DirectShow
ms.assetid: 8973281f-2037-487f-9e86-8c7ceca75b23
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_TVFormat method, IAMAnalogVideoDecoder.get_TVFormat, IAMAnalogVideoDecoder::get_TVFormat, IAMAnalogVideoDecoderget_TVFormat, dshow.iamanalogvideodecoder_get_tvformat, get_TVFormat, get_TVFormat method [DirectShow], get_TVFormat method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_TVFormat
ms.topic: method
f1_keywords: 
 - "strmif/IAMAnalogVideoDecoder.get_TVFormat"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMAnalogVideoDecoder.get_TVFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMAnalogVideoDecoder::get_TVFormat


## -description



The <code>get_TVFormat</code> method retrieves the current analog video format.




## -parameters




### -param plAnalogVideoStandard [out]

Pointer to a variable that receives a member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard</a> enumeration, indicating the analog video format.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamanalogvideodecoder">IAMAnalogVideoDecoder Interface</a>
 

 

