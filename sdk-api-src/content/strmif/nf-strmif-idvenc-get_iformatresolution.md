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

# IDVEnc::get_IFormatResolution


## -description



The <b>get_IFormatResolution</b> method retrieves the encoding resolution.




## -parameters




### -param VideoFormat [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/14f32314-96f4-4880-a141-89cf6e66ed6c">DVENCODERVIDEOFORMAT</a> enumeration, specifying the video standard in use (NTSC or PAL).


### -param DVFormat [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/462c8034-5931-435d-8f18-b58842f2e234">DVENCODERFORMAT</a> enumeration, specifying the digital video (DV) format.


### -param Resolution [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/110a4510-3a5e-453b-9973-a6cf7e2b0050">DVENCODERRESOLUTION</a> enumeration, specifying the video resolution.


### -param fDVInfo [in]

Boolean value specifying whether to retrieve the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559517">DVINFO</a> structure that specifies the stream format. If <b>TRUE</b>, the stream format is returned in the <i>sDVInfo</i> parameter.


### -param sDVInfo [out]

Pointer to a variable that receives a <b>DVINFO</b> structure containing the stream format. If <i>fDVInfo</i> is <b>FALSE</b>, this parameter is ignored.


## -returns



Returns S_OK if successful. Otherwise, returns E_FAIL or another error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f193b76f-ca6a-44f5-b097-1570c4527ab4">IDVEnc Interface</a>
 

 

