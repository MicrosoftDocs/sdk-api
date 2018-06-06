---
UID: NF:strmif.IAMAnalogVideoDecoder.get_TVFormat
title: IAMAnalogVideoDecoder::get_TVFormat
author: windows-sdk-content
description: The get_TVFormat method retrieves the current analog video format.
old-location: dshow\iamanalogvideodecoder_get_tvformat.htm
old-project: DirectShow
ms.assetid: 8973281f-2037-487f-9e86-8c7ceca75b23
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMAnalogVideoDecoder interface [DirectShow],get_TVFormat method, IAMAnalogVideoDecoder.get_TVFormat, IAMAnalogVideoDecoder::get_TVFormat, IAMAnalogVideoDecoderget_TVFormat, dshow.iamanalogvideodecoder_get_tvformat, get_TVFormat, get_TVFormat method [DirectShow], get_TVFormat method [DirectShow],IAMAnalogVideoDecoder interface, strmif/IAMAnalogVideoDecoder::get_TVFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoDecoder::get_TVFormat


## -description



The <code>get_TVFormat</code> method retrieves the current analog video format.




## -parameters




### -param plAnalogVideoStandard [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration, indicating the analog video format.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/81d43941-7c81-4220-915f-0b373a7455e5">IAMAnalogVideoDecoder Interface</a>
 

 

