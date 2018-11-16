---
UID: NF:strmif.IAMAnalogVideoEncoder.put_CopyProtection
title: IAMAnalogVideoEncoder::put_CopyProtection
author: windows-sdk-content
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The put_CopyProtection method sets the level of copy protection for the encoder.
old-location: dshow\iamanalogvideoencoder_put_copyprotection.htm
tech.root: DirectShow
ms.assetid: a2a762f3-8b11-4334-979d-206234d6cf09
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],put_CopyProtection method, IAMAnalogVideoEncoder.put_CopyProtection, IAMAnalogVideoEncoder::put_CopyProtection, IAMAnalogVideoEncoderput_CopyProtection, dshow.iamanalogvideoencoder_put_copyprotection, put_CopyProtection, put_CopyProtection method [DirectShow], put_CopyProtection method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::put_CopyProtection
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
 - IAMAnalogVideoEncoder.put_CopyProtection
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
- IAMAnalogVideoEncoder.put_CopyProtection
: 
---

# IAMAnalogVideoEncoder::put_CopyProtection


## -description



<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>put_CopyProtection</code> method sets the level of copy protection for the encoder.




## -parameters




### -param lVideoCopyProtection [in]

Specifies the level of copy protection as a <b>long</b> integer with a value as defined in the <a href="https://msdn.microsoft.com/d71f78f4-1107-46ba-afa8-7de87e20d814">AM_COPY_MACROVISION_LEVEL</a> enumeration.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fb2927cf-c979-411f-a896-d010b684acf2">IAMAnalogVideoEncoder Interface</a>
 

 

