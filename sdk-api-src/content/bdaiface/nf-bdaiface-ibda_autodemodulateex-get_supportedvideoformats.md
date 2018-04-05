---
UID: NF:bdaiface.IBDA_AutoDemodulateEx.get_SupportedVideoFormats
title: IBDA_AutoDemodulateEx::get_SupportedVideoFormats method
author: windows-driver-content
description: The get_SupportedVideoFormats method retrieves the video formats that are supported by the demodulator.
old-location: mstv\ibda_autodemodulateex_get_supportedvideoformats.htm
old-project: mstv
ms.assetid: bba4a57c-7e07-45ca-84d0-921caf39f345
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IBDA_AutoDemodulateEx, IBDA_AutoDemodulateEx interface [Microsoft TV Technologies], get_SupportedVideoFormats method, IBDA_AutoDemodulateEx::get_SupportedVideoFormats, IBDA_AutoDemodulateExget_SupportedVideoFormats, bdaiface/IBDA_AutoDemodulateEx::get_SupportedVideoFormats, get_SupportedVideoFormats method [Microsoft TV Technologies], get_SupportedVideoFormats method [Microsoft TV Technologies], IBDA_AutoDemodulateEx interface, get_SupportedVideoFormats,IBDA_AutoDemodulateEx.get_SupportedVideoFormats, mstv.ibda_autodemodulateex_get_supportedvideoformats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bdaiface.h
api_name:
-	IBDA_AutoDemodulateEx.get_SupportedVideoFormats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_AutoDemodulateEx::get_SupportedVideoFormats method


## -description


The <b>get_SupportedVideoFormats</b> method retrieves the video formats that are supported by the demodulator.


## -parameters




### -param pulAMTunerModeType [out]

Pointer to a variable that receives a mask that indicates the frequency ranges that are supported by the BDA device filter. For a list of valid mask bits, see <a href="https://msdn.microsoft.com/ce5e6f6d-da79-4a86-abd4-bb28e66d5947">AMTunerModeType Enumeration</a>.


### -param pulAnalogVideoStandard [out]

Pointer to a variable that receives a mask that indicates the analog television signal formats that are supported by the BDA device filter. For a list of valid mask bits, see <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard Enumeration</a>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/ecc642e4-7c36-400c-8a63-639f75b2bbc2">IBDA_AutoDemodulateEx Interface</a>
 

 

