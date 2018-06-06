---
UID: NF:strmif.IAMAnalogVideoEncoder.put_TVFormat
title: IAMAnalogVideoEncoder::put_TVFormat
author: windows-sdk-content
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The put_TVFormat method sets the encoder to a particular analog video standard (NTSC/M, PAL/B, SECAM/K1, and so on).
old-location: dshow\iamanalogvideoencoder_put_tvformat.htm
old-project: DirectShow
ms.assetid: 76109fa1-2f7a-4538-9755-6e2de5852d4b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],put_TVFormat method, IAMAnalogVideoEncoder.put_TVFormat, IAMAnalogVideoEncoder::put_TVFormat, IAMAnalogVideoEncoderput_TVFormat, dshow.iamanalogvideoencoder_put_tvformat, put_TVFormat, put_TVFormat method [DirectShow], put_TVFormat method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::put_TVFormat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAnalogVideoEncoder.put_TVFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoEncoder::put_TVFormat


## -description



<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>put_TVFormat</code> method sets the encoder to a particular analog video standard (NTSC/M, PAL/B, SECAM/K1, and so on).




## -parameters




### -param lAnalogVideoStandard [in]

Specifies the video standard to set in the encoder as a <b>long</b> integer containing a value as defined in the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fb2927cf-c979-411f-a896-d010b684acf2">IAMAnalogVideoEncoder Interface</a>
 

 

