---
UID: NF:strmif.IDVEnc.get_IFormatResolution
title: IDVEnc::get_IFormatResolution (strmif.h)
author: windows-sdk-content
description: The get_IFormatResolution method retrieves the encoding resolution.
old-location: dshow\idvenc_get_iformatresolution.htm
tech.root: DirectShow
ms.assetid: 5921e19a-d500-4799-88a0-ff2f67bd81af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVEnc interface [DirectShow],get_IFormatResolution method, IDVEnc.get_IFormatResolution, IDVEnc::get_IFormatResolution, IDVEncget_IFormatResolution, dshow.idvenc_get_iformatresolution, get_IFormatResolution, get_IFormatResolution method [DirectShow], get_IFormatResolution method [DirectShow],IDVEnc interface, strmif/IDVEnc::get_IFormatResolution
ms.topic: method
f1_keywords: ["strmif/IDVEnc.get_IFormatResolution"]
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
 - IDVEnc.get_IFormatResolution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVEnc::get_IFormatResolution


## -description



The <b>get_IFormatResolution</b> method retrieves the encoding resolution.




## -parameters




### -param VideoFormat [out]

Pointer to a variable that receives a member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_dvencodervideoformat">DVENCODERVIDEOFORMAT</a> enumeration, specifying the video standard in use (NTSC or PAL).


### -param DVFormat [out]

Pointer to a variable that receives a member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_dvencoderformat">DVENCODERFORMAT</a> enumeration, specifying the digital video (DV) format.


### -param Resolution [out]

Pointer to a variable that receives a member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_dvencoderresolution">DVENCODERRESOLUTION</a> enumeration, specifying the video resolution.


### -param fDVInfo [in]

Boolean value specifying whether to retrieve the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvinfo">DVINFO</a> structure that specifies the stream format. If <b>TRUE</b>, the stream format is returned in the <i>sDVInfo</i> parameter.


### -param sDVInfo [out]

Pointer to a variable that receives a <b>DVINFO</b> structure containing the stream format. If <i>fDVInfo</i> is <b>FALSE</b>, this parameter is ignored.


## -returns



Returns S_OK if successful. Otherwise, returns E_FAIL or another error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvenc">IDVEnc Interface</a>
 

 

