---
UID: NF:strmif.IDVEnc.put_IFormatResolution
title: IDVEnc::put_IFormatResolution (strmif.h)
author: windows-sdk-content
description: The put_IFormatResolution method sets the encoding resolution.
old-location: dshow\idvenc_put_iformatresolution.htm
tech.root: DirectShow
ms.assetid: c9cf2544-1b04-4a77-8a0b-d7820af5ff9f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDVEnc interface [DirectShow],put_IFormatResolution method, IDVEnc.put_IFormatResolution, IDVEnc::put_IFormatResolution, IDVEncput_IFormatResolution, dshow.idvenc_put_iformatresolution, put_IFormatResolution, put_IFormatResolution method [DirectShow], put_IFormatResolution method [DirectShow],IDVEnc interface, strmif/IDVEnc::put_IFormatResolution
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
---

# IDVEnc::put_IFormatResolution


## -description



The <code>put_IFormatResolution</code> method sets the encoding resolution.




## -parameters




### -param VideoFormat [in]

Member of the <a href="https://msdn.microsoft.com/14f32314-96f4-4880-a141-89cf6e66ed6c">DVENCODERVIDEOFORMAT</a> enumeration, specifying the video standard to use (NTSC or PAL).


### -param DVFormat [in]

Member of the <a href="https://msdn.microsoft.com/462c8034-5931-435d-8f18-b58842f2e234">DVENCODERFORMAT</a> enumeration, specifying the DV format.


### -param Resolution [in]

Member of the <a href="https://msdn.microsoft.com/110a4510-3a5e-453b-9973-a6cf7e2b0050">DVENCODERRESOLUTION</a> enumeration, specifying the video resolution.


### -param fDVInfo [in]

Boolean value specifying whether the <i>sDVInfo</i> parameter contains a valid <a href="https://msdn.microsoft.com/285a56fc-9c25-4c5a-ae6a-146c17b00e84">DVINFO</a> structure. To set the stream format, set this parameter to <b>TRUE</b> and specify the format chunk with the <i>sDVInfo</i> parameter.


### -param sDVInfo [in]

If <i>fDVInfo</i> is <b>TRUE</b>, must point to a <b>DVINFO</b> structure that describes the stream format.


## -returns



Returns S_OK if successful. Otherwise, returns E_FAIL or another error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f193b76f-ca6a-44f5-b097-1570c4527ab4">IDVEnc Interface</a>
 

 

