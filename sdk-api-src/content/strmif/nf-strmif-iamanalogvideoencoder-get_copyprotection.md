---
UID: NF:strmif.IAMAnalogVideoEncoder.get_CopyProtection
title: IAMAnalogVideoEncoder::get_CopyProtection
author: windows-sdk-content
description: Note  The IAMAnalogVideoEncoder interface is deprecated. The get_CopyProtection method determines whether copy protection is currently enabled on the encoder.
old-location: dshow\iamanalogvideoencoder_get_copyprotection.htm
tech.root: DirectShow
ms.assetid: 3eedb123-c70e-4a9a-98a9-abf7ccad32dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMAnalogVideoEncoder interface [DirectShow],get_CopyProtection method, IAMAnalogVideoEncoder.get_CopyProtection, IAMAnalogVideoEncoder::get_CopyProtection, IAMAnalogVideoEncoderget_CopyProtection, dshow.iamanalogvideoencoder_get_copyprotection, get_CopyProtection, get_CopyProtection method [DirectShow], get_CopyProtection method [DirectShow],IAMAnalogVideoEncoder interface, strmif/IAMAnalogVideoEncoder::get_CopyProtection
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
 - IAMAnalogVideoEncoder.get_CopyProtection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMAnalogVideoEncoder::get_CopyProtection


## -description



<div class="alert"><b>Note</b>  The <b>IAMAnalogVideoEncoder</b> interface is deprecated.</div>
<div> </div>
The <code>get_CopyProtection</code> method determines whether copy protection is currently enabled on the encoder.




## -parameters




### -param lVideoCopyProtection [out]

Specifies a pointer to a <b>long</b> integer to receive the current copy protection level, as defined in the <a href="https://msdn.microsoft.com/d71f78f4-1107-46ba-afa8-7de87e20d814">AM_COPY_MACROVISION_LEVEL</a> enumeration.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b>




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/fb2927cf-c979-411f-a896-d010b684acf2">IAMAnalogVideoEncoder Interface</a>
 

 

