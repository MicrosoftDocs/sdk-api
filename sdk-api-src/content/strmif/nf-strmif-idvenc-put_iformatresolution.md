---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

Boolean value specifying whether the <i>sDVInfo</i> parameter contains a valid <a href="https://msdn.microsoft.com/library/windows/hardware/ff559517">DVINFO</a> structure. To set the stream format, set this parameter to <b>TRUE</b> and specify the format chunk with the <i>sDVInfo</i> parameter.


### -param sDVInfo [in]

If <i>fDVInfo</i> is <b>TRUE</b>, must point to a <b>DVINFO</b> structure that describes the stream format.


## -returns



Returns S_OK if successful. Otherwise, returns E_FAIL or another error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f193b76f-ca6a-44f5-b097-1570c4527ab4">IDVEnc Interface</a>
 

 

