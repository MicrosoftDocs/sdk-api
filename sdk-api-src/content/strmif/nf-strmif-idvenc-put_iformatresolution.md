---
UID: NF:strmif.IDVEnc.put_IFormatResolution
title: IDVEnc::put_IFormatResolution (strmif.h)
author: windows-sdk-content
description: The put_IFormatResolution method sets the encoding resolution.
old-location: dshow\idvenc_put_iformatresolution.htm
tech.root: DirectShow
ms.assetid: c9cf2544-1b04-4a77-8a0b-d7820af5ff9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVEnc interface [DirectShow],put_IFormatResolution method, IDVEnc.put_IFormatResolution, IDVEnc::put_IFormatResolution, IDVEncput_IFormatResolution, dshow.idvenc_put_iformatresolution, put_IFormatResolution, put_IFormatResolution method [DirectShow], put_IFormatResolution method [DirectShow],IDVEnc interface, strmif/IDVEnc::put_IFormatResolution
ms.topic: method
f1_keywords: 
 - "strmif/IDVEnc.put_IFormatResolution"
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
 - IDVEnc.put_IFormatResolution
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVEnc::put_IFormatResolution


## -description



The <code>put_IFormatResolution</code> method sets the encoding resolution.




## -parameters




### -param VideoFormat [in]

Member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_dvencodervideoformat">DVENCODERVIDEOFORMAT</a> enumeration, specifying the video standard to use (NTSC or PAL).


### -param DVFormat [in]

Member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_dvencoderformat">DVENCODERFORMAT</a> enumeration, specifying the DV format.


### -param Resolution [in]

Member of the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_dvencoderresolution">DVENCODERRESOLUTION</a> enumeration, specifying the video resolution.


### -param fDVInfo [in]

Boolean value specifying whether the <i>sDVInfo</i> parameter contains a valid <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvinfo">DVINFO</a> structure. To set the stream format, set this parameter to <b>TRUE</b> and specify the format chunk with the <i>sDVInfo</i> parameter.


### -param sDVInfo [in]

If <i>fDVInfo</i> is <b>TRUE</b>, must point to a <b>DVINFO</b> structure that describes the stream format.


## -returns



Returns S_OK if successful. Otherwise, returns E_FAIL or another error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvenc">IDVEnc Interface</a>
 

 

