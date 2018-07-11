---
UID: NF:strmif.IAMAnalogVideoEncoder.get_AvailableTVFormats
title: IAMAnalogVideoEncoder::get_AvailableTVFormats
author: windows-sdk-content
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The get_AvailableTVFormats method retrieves the analog video standards (NTSC/M, PAL/B, SECAM/K1, and so on) supported by the encoder.
old-location: dshow\iamanalogvideoencoder_get_availabletvformats.htm
old-project: DirectShow
ms.assetid: 739a5f6f-2498-49f4-9c9d-008bd71d4855
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],get_AvailableTVFormats method, IAMAnalogVideoEncoder.get_AvailableTVFormats, IAMAnalogVideoEncoder::get_AvailableTVFormats, IAMAnalogVideoEncoderget_AvailableTVFormats, dshow.iamanalogvideoencoder_get_availabletvformats, get_AvailableTVFormats, get_AvailableTVFormats method [DirectShow], get_AvailableTVFormats method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::get_AvailableTVFormats
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
 - IAMAnalogVideoEncoder.get_AvailableTVFormats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAnalogVideoEncoder::get_AvailableTVFormats


## -description



<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>get_AvailableTVFormats</code> method retrieves the analog video standards (NTSC/M, PAL/B, SECAM/K1, and so on) supported by the encoder.




## -parameters




### -param lAnalogVideoStandard [out]

Specifies a pointer to a <b>long</b> integer to receive the available TV formats. The formats are defined in the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration and the available formats have been combined in this integer with a bitwise OR.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fb2927cf-c979-411f-a896-d010b684acf2">IAMAnalogVideoEncoder Interface</a>
 

 

