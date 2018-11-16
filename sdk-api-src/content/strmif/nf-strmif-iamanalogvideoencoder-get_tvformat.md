---
UID: NF:strmif.IAMAnalogVideoEncoder.get_TVFormat
title: IAMAnalogVideoEncoder::get_TVFormat
author: windows-sdk-content
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The get_TVFormat method retrieves the analog video standard that the encoder is currently set to (NTSC/M, PAL/B, SECAM/K1, and so on).
old-location: dshow\iamanalogvideoencoder_get_tvformat.htm
tech.root: DirectShow
ms.assetid: 5a88e2e7-508b-448b-ac1d-50a50b4bb79a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],get_TVFormat method, IAMAnalogVideoEncoder.get_TVFormat, IAMAnalogVideoEncoder::get_TVFormat, IAMAnalogVideoEncoderget_TVFormat, dshow.iamanalogvideoencoder_get_tvformat, get_TVFormat, get_TVFormat method [DirectShow], get_TVFormat method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::get_TVFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAnalogVideoEncoder.get_TVFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMAnalogVideoEncoder.get_TVFormat
: 
---

# IAMAnalogVideoEncoder::get_TVFormat


## -description



<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>get_TVFormat</code> method retrieves the analog video standard that the encoder is currently set to (NTSC/M, PAL/B, SECAM/K1, and so on).




## -parameters




### -param plAnalogVideoStandard [out]

Specifies a pointer to a <b>long</b> integer to receive the encoder's current video standard.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



Possible values and their meaning are defined in the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fb2927cf-c979-411f-a896-d010b684acf2">IAMAnalogVideoEncoder Interface</a>
 

 

